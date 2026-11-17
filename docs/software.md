---
layout: page
title: Computer and Software
permalink: /software/
---

## Computer Software

### Setting up a new station

You have a USB stick and a small computer with a radio receiver attached. About an hour from now the machine will record and decode HF signals on its own. It sends nothing to the outside world until you have checked it and said so. Read the first section before you touch anything: it is the only part that needs preparation.

**This erases the computer's internal disk.** Everything on it goes, with no further warning once you boot from the stick. Use a machine you intend to dedicate to this.

### 1 · Collect these first

The setup wizard asks for these after the machine has installed itself. Written down in advance, they take two minutes to type. Only the first two are required.

| **The wizard asks, in this order** | **Looks like**                                                                                | **Yours** |
| :--------------------------------- | :-------------------------------------------------------------------------------------------- | :-------- |
| **Reporter ID**<br>required        | AC0G/B4<br>your callsign; a suffix after the slash tells apart several stations you run       |           |
| **Grid square**<br>required        | EM38ww<br>not asked at all if the GPS clock already has a fix                                 |           |
| Antenna description                | 80 m dipole at 40 ft<br>optional, free text                                                   |           |
| Wi-Fi network and passphrase       | only if you will run without a network cable<br>asked only when the machine has a Wi-Fi radio |           |
| DASI station? Its unit number      | Y, then 3 (for DASI-003)<br>only for HamSCI DASI stations                                     |           |
| **PSWS station ID**                | S000170<br>the letter S and six digits, from your PSWS account; Enter skips PSWS              |           |
| **GRAPE instrument ID**            | 171<br>the receiver, as numbered on the PSWS portal                                           |           |
| **Magnetometer instrument number** | 84<br>only if you have a magnetometer; it reports under the same station ID                   |           |
| Status heartbeats                  | Y<br>press Enter to accept the collector it offers                                            |           |
| Station designator                 | AC0G-B4<br>offered from your reporter ID; press Enter to accept                               |           |

**Names beginning DASI and three digits are reserved** for the NSF-funded DASI2 fleet and checked against a roster that ships with the software. If you were issued one, use exactly that; your PSWS IDs come from the roster. A DASI name that is not in the roster gets refused rather than guessed at: check for a typo, or ask your fleet admin.

**No PSWS account yet?** Press Enter at the PSWS station ID. The station records and works; PSWS uploads start once you add the IDs and register the station's key.

### And physically, before you begin

- A mini-PC with **16 GB of RAM or more** and an internal **NVMe** drive. The installer writes only to an NVMe drive.
- The **RX888 Mk2 receiver and the LBE-1421 GPS clock** plugged in and powered before the first boot. A magnetometer, a TS-1 time injector or a local GPS time server, if you have one, can plug in now too; the station finds them by itself. Anything missing does not stop the install; you can add it later.
- A USB stick of **16 GB or more**. It gets overwritten.
- A screen and keyboard on the machine, until the wizard finishes.
- A network: a cable to your router (the machine takes its address automatically), or a Wi-Fi network you join during setup. Sites with only IPv6 work too.

### 2 · Get the image and write the stick

Your fleet admin sends you two files, or download links for them: the image, sigmond-appliance-v3.78-20261021-release.img (about 5.6 GB), and its checksum, …release.sha256. A later release carries its own version and date in the name; use the names you were given. Keep both in one folder and check the image:

```
sha256sum -c sigmond-appliance-v3.78-20261021-release.sha256
```

The image is **not compressed**: there is nothing to unzip.

With the project's tools, this is the safe way to write it. It finds the stick by looking for something removable, *refuses* the disk your own computer runs from, and reads the stick back afterwards to check every byte:

```
./flash-usb.sh sigmond-appliance-v3.78-20261021-release.img
```

balenaEtcher or Raspberry Pi Imager ("Use custom") work too, and both verify the write. By hand, with only the image file:

```
lsblk -dno NAME,SIZE,TRAN,RM,MODEL        # find the stick, check its size
sudo dd if=sigmond-appliance-v3.78-20261021-release.img of=/dev/sdX bs=4M \
        oflag=direct conv=fsync status=progress
sync
```

Getting /dev/sdX wrong overwrites that computer's own disk, immediately and without asking. Check the size and that it says removable before you press Enter.

Afterwards your computer may show one small drive from the stick, often named "EFI" or "NO NAME". That is normal.

### 3 · Install

### Boot from the stick

With the receiver connected, power on and boot from the USB stick: press the boot-menu key as it starts (usually F7, F11, F12 or Del) and pick the USB entry. If no menu appears, turn **Fast Boot off** in the BIOS setup. The installer then runs **by itself**, asking nothing. This is when the internal disk gets erased.

**It can sit on "creating LVs" for a long time** when the disk held an earlier install. The installer is working, not hung. Wait at least 30 minutes before you consider switching it off; cutting power there only makes you start again.

#### Wait for it to switch itself off

After a few minutes the machine **powers off**. That is the signal, not a failure.

**Remove the stick, then switch the machine back on.** The power-off is deliberate: some machines always boot from USB first, and would otherwise install again in a loop.

When it comes back up, the screen says the host is running and gives its address, its login, and the next step:

NEXT STEP: plug in the Sigmond install USB stick. The decoder VM then installs itself automatically.

#### Put the stick back in

Insert **the same stick** again, into any port, and leave it in. The screen answers:

&#x20;Sigmond USB detected (…).  Importing the decoder VM (\~3 min). LEAVE THE STICK IN.

### Answer the wizard

The setup questions appear on the screen. **Leave the stick in.**

1. First the wizard lists the equipment it found: receiver, GPS clock, TS-1, magnetometer. Missing items do not stop it.
2. Then it asks the questions from your sheet, in the order of the table above. Press Enter to accept a suggestion or to skip an optional item.
3. A **review screen** shows every answer. Type a line number to change one, or **Y** to apply.

Saying yes to heartbeats lets a dashboard show that your station is alive and healthy. It sends a small report every five minutes, outbound only, and opens nothing on your machine.

**Remote access comes up by itself.** The wizard asks nothing about it: every station registers with the fleet gateway and opens a tunnel, so that your fleet admin can support it. Registering sends two things: the station's name and the host's public key. You hold the switch, and section 6, Logins and the password, says how to work it.

#### Remove the stick; it powers off

The machine now tunes itself: it reserves processor cores for the receiver and hands it the USB ports. Then it says:

&#x20;\>>> INSTALL COMPLETE — REMOVE THE USB STICK NOW <<<  As soon as the stick is removed this machine POWERS OFF.

**Pull the stick. The machine switches off. Switch it back on.** That full power-off also resets the receiver, which it needs.

#### Let it finish building

After you power it on, the screen shows a status panel. While the panel says **STATION IS STILL BUILDING**, leave it alone: on a fresh machine that can take tens of minutes. The panel also shows every address and login you need next. From here on you use the station from another computer.

### 4 · Check it, then turn on uploads

**A new station starts with its site sink switch at off.** It records and decodes, but sends no spots or data to wsprnet, pskreporter.info, wsprdaemon.org or PSWS. Only its heartbeat, the five-minute health report, goes out. That way nothing leaves until you know the station hears well and reports the right callsign and grid.

### Ask the station how it stands

About fifteen minutes after the panel stops saying it is building, press Enter at the station's keyboard and log in to the host (see section 6). Then type one command:

```
sigmond-check
```

It takes about fifteen seconds. It prints one line for each part of the station and ends with a verdict:

```
 ok    PSK            214 FT8 and 31 FT4 spots in the last 15 min
 ok    WSPR           48 spots in the last 10 min, on 6 bands
 FAIL  magnetometer   frozen: 0.00 C, no change in 60 s.
                      Fix: sigmond-vm sudo systemctl restart mag-recorder
 wait  GRAPE          first files due in about 7 min (hf-timestd started 4 min ago)
 ok    storage        /var/lib has 61 % free
 wait  uploads        off, new station: check the lines above, then run: sigmond-vm smd sink upload
 --    meteor scatter not on this station
 ok    receiver page  IPv4 http://192.168.1.50:8081   IPv6 http://[2601:db8::50]:8081
 ok    station pages  IPv4 http://192.168.1.50:8000   IPv6 http://[2601:db8::50]:8000
 ok    magnetometer page  IPv4 http://192.168.1.50:8082   IPv6 http://[2601:db8::50]:8082
FAIL  (1 failing, 2 waiting)
```

The word at the start of each line tells you how that part stands:

| **Word** | **Meaning**                                                                            |
| :------- | :------------------------------------------------------------------------------------- |
| ok       | It works.                                                                              |
| wait     | Not yet. A new station shows this for a while; the line usually says how long to wait. |
| FAIL     | It does not work. The line says what to do, or whom to tell.                           |
| --       | This station does not run that part, and the verdict leaves it out.                    |

The last line gives the verdict. PASS means every part works. WAIT means some part has not started yet: wait the time its line names, then type sigmond-check again. FAIL means some part does not work. A fix stands on its own line under it, after the word Fix:; type it exactly as printed. When a FAIL line names no fix, send the whole output to your fleet admin.

Right after the install the station may still bring itself up; then the first line reads wait  bring-up. If it reads FAIL  bring-up  ran without the radio, no SDR stood on the USB bus. Plug the SDR in, and bring-up finishes by itself. A quiet band can look like a fault, so a line that reports no spots asks you to check the antenna and its cable first.

The page lines print the addresses to open from another computer on the same network: the receiver's waterfall, the station pages with your callsign and grid, and the magnetometer's readings. A browser needs square brackets around an IPv6 address. These pages answer only computers on the station's own network. A computer elsewhere on the internet, or a VPN peer of the host, gets no answer.

#### Raise the site sink switch

A new station's uploads line reads wait and says new station. When every other line shows ok or --, turn uploads on, still at the host's login:

```
sigmond-vm smd sink upload
sigmond-check       # the uploads line shows ok after the first delivery, within 30 minutes
```

An uploads line that shows FAIL with off or hold and some other reason means someone set the switch on purpose: leave it alone and ask your fleet admin. About fifteen minutes after you turn uploads on, search your reporter ID at wsprnet.org (Database) and your callsign at pskreporter.info.

**What ships, and when.** When you run smd sink upload, the station sends the GRAPE and magnetometer packages for today and yesterday (UTC), even if it built them while the switch read off. Older packages stay on the station, and nothing else recorded before the switch ships. The station packs each UTC day's data after that day ends, between 01:00 and about 05:00 UTC; a package not built yet goes out once the station builds it. While a packing job runs, smd sink upload refuses, names the job, and asks you to try again when it ends.

### 5 · Things that look wrong and are not

| **You see**                                                                                    | **What it means**                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                                        |
| :--------------------------------------------------------------------------------------------- | :--------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| The machine switches itself off, twice                                                         | Both are expected: once after the first install, once after you remove the stick at the end. Power it on each time.                                                                                                                                                                                                                                                                                                                                                                                                                      |
| It asks for the stick a second time                                                            | Expected. The first boot installs the host; the second loads the recording system.                                                                                                                                                                                                                                                                                                                                                                                                                                                       |
| The keyboard no longer types into the host                                                     | Normal. The USB ports now belong to the recorder, so a keyboard on the machine types into the recorder. The screen's second line says what it still does: Press Enter here for a hypervisor login; typing does not echo, which is normal. Press Enter, then type the host's root password when the screen asks; nothing shows while you type it. With that login on the host you can type sigmond-setup --rac-off, sigmond-setup --rac-on and sigmond-setup --pair-vm. For everything else, use SSH or a web page from another computer. |
| No spots on wsprnet or pskreporter                                                             | Expected until you run smd sink upload (section 4). If smd sink status already says upload, check that the antenna is connected, then run smd status and send its output to your fleet admin.                                                                                                                                                                                                                                                                                                                                            |
| "no RX888" or other missing equipment                                                          | The station installs and waits. Plug the RX888 into a **blue** USB 3 port, straight into the machine with no hub. Then run sigmond-vm smd status on the host and sigmond-vm smd adopt \<name> with the name it printed. Nothing starts until you ask.                                                                                                                                                                                                                                                                                    |
| The receiver shows up, but nothing decodes and the log says RX888 ADC clock not locked/running | Unplug the USB 3 cable **at the RX888** and plug it firmly back in. A badly seated plug looks exactly like a missing clock, and a power cycle does not cure it.                                                                                                                                                                                                                                                                                                                                                                          |
| Remote access says "wanted on, not up"                                                         | The station works. smd remote status on the recorder names the case on its second line. "has not registered yet" means no gateway has answered; the host tries again every ten minutes.                                                                                                                                                                                                                                                                                                                                                  |
| The screen says ssh root@\<host> 'sigmond-setup --rac-off' where this page says smd remote off | The recorder and the host have not paired yet, or the host's last check of the pairing failed. Type the screen's line from another computer; it works the same switch.                                                                                                                                                                                                                                                                                                                                                                   |
| The screen says bring-up ran WITHOUT the radio                                                 | No SDR stood on the USB bus when the build ran. Plug the SDR in. The build finishes by itself, and nothing else needs your hands.                                                                                                                                                                                                                                                                                                                                                                                                        |
| The screen says the decoder VM's guest agent does not answer                                   | The host cannot ask the recorder anything for the moment. The radio and the uploads go on. The screen tries a reset every five minutes. If the line stays for more than ten minutes while the recorder runs, tell your fleet admin.                                                                                                                                                                                                                                                                                                      |

#### If it says the install cannot continue

A block on the screen beginning INSTALL CANNOT CONTINUE NORMALLY means the machine found no working network. Its title says which case: **no network cable detected**, **the port is connected but nothing answered**, or **no address offered**. The block lists three ways out:

1. Move the cable to a port whose link light is on, then reboot.
2. Give it a fixed address: sigmond-setnet 10.0.0.50/24 10.0.0.1 (your address and router).
3. Use Wi-Fi instead: sigmond-wifi scan, then join your network with sigmond-wifi join YourNetwork, giving the passphrase as the screen shows.

#### 6 · Logins and the password

The status panel on the machine's screen lists everything below with your real addresses filled in.

| **What**                  | **How**                                                                                                                                                                                                  |
| :------------------------ | :------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------- |
| The host (Proxmox)        | ssh root@\<host>, or the web page https\://\<host>:8006                                                                                                                                                  |
| The recorder (decoder VM) | ssh -p 2222 sigmond@\<host>, relayed by the host (also hamsci@). On a station with the old layout, where the recorder sits on your own network with no private link to the host: ssh sigmond@\<recorder> |

**One password for the whole station.** It starts as hamsci-sigmond. The wizard copies the host's root password to the recorder's accounts, so the recorder accepts the same one. **Change it**: run passwd on the host and on the recorder. Root login over SSH on the recorder stays off.

### Turning remote access off and on

Remote access starts on. To change that, log in to the recorder and type:

```
smd remote off        turn it off; it stays off across reboots
smd remote on         turn it on again
smd remote status     show the state
```

Off stops the tunnel your fleet admin uses and changes nothing else: every upload keeps running. The status panel on the machine's screen shows which state holds.

### Register for PSWS uploads

If you gave PSWS IDs, log in to the recorder. Its login banner shows this machine's public upload key. Paste that key into the PSWS portal for your station (pswsnetwork.eng.ua.edu), then run:

```
smd psws verify
```

Until the key verifies, the station keeps recording. Packages built after you run smd sink upload wait on the station and ship once the key verifies; packages built before that command stay in a held folder on the station and never ship. **One key serves the whole machine:** if it uploads for more than one station, register the same key on each of them.

#### 7 · Replacing an existing station?

Its upload keys can travel on the stick, so you need not register again.

1. On the old machine: tar czf site-keys.tar.gz -C / etc/hs-uploader/keys home/timestd/.ssh
2. After writing the stick, your computer shows one small drive from it. Copy site-keys.tar.gz onto it and eject.
3. Install as above. The wizard restores the keys and, if you gave PSWS IDs, checks the PSWS login for you.

#### 8 · Moving a station

A station often gets built and tested in one place, with the wrong grid square, and then shipped to its permanent home. Keep the site sink switch at off until the station knows where it stands.

1. At the staging site, leave the switch at off; a new station starts that way. Check reception with the waterfall and smd watch wspr. Only the heartbeat goes out.
2. At the destination, log in to the host and run sigmond-setup --reconfigure.
3. Answer the questions again. The wizard asks for your reporter ID and PSWS IDs afresh, and Enter at the PSWS station ID skips PSWS, so have them at hand. Type the **new grid square**. A GPS clock with a fix fills in the grid by itself and may already have changed it; check it on the review screen. The wizard keeps your remote-access number, the remote-access switch and the site sink switch as they were, and restarts the recorders itself.
4. On the recorder, check the identity with grep -E 'reporter_id|callsign|grid' /etc/sigmond/site-profile.toml, then run smd sink status. With the reason new station: …, run smd sink upload. If it already says upload, someone raised it earlier. Any other reason, or hold (legacy): ask your fleet admin. Check wsprnet about fifteen minutes later.

---

For sigmond-appliance v3.78, blessed 2026-10-22. The steps, screen messages and logins here follow the release's installation guide. The image builder's nested test installed v3.78 from scratch, its update test carried a v3.73 station forward and back, and AC0G-B4 installed v3.78 from scratch on hardware. No IPv6-only site has installed it from scratch yet. Day-2 operation, health checks and troubleshooting live in the operator guide: github.com/HamSCI/sigmond/blob/main/docs/operator/README.md
