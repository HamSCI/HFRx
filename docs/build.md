---
layout: page
title: Build
permalink: /build/
---

**Release:** draft · **Date:** 2026-11-17 · **Authors:** Santino Gregorovic, Jason Lai, Sanika Chaturvedi · **License:** to be decided

<!-- ## and ### headings appear in sidebar automatically (limit set in sidebar.html)-->

## Assembly

### Build Receiver

_text_

#### heading 4 

_text_

<!--
Sources used:
  [DXE]  DX Engineering DXE-RSEAV-1 manual
  [ARC]  Archive page (old info)
  [K3]   K3DFD-PSWS hardware.md
  [CAP]  Senior team Antenna Build Capture
Lines marked FLAG need a team decision or more information before release

There will be a esparate page that identifies flagS
-->

## Install the antenna

This part installs the DX Engineering DXE-RSEAV-1 active receive antenna. At the end, the antenna is on a ground rod, grounded, and powered through a separate DC cable.

The work has seven tasks:

1. Set the power jumpers in the matching unit.
2. Assemble the matching unit and clamps on the mounting plate.
3. Attach the bottom element to the mounting plate.
4. Install the ground rod and the ground clamp.
5. Mount the antenna on the ground rod.
6. Install the middle and top elements.
7. Connect the RF coax and the DC power.

<!-- FLAG (optional): Consider a connection diagram (antenna, RF coax, DC cable, ground rod, receiver). No rule requires one. If added, follow F-6 to F-8. -->

### Before you start

#### Safety

Read these messages before you start.

> **⚠ DANGER** Overhead power lines. Keep the antenna and ground rod away from overhead power lines and other electric circuits. Contact with these circuits can cause serious injury or death.
{: .callout-danger}

> **NOTICE** Receive-only antenna. Never transmit through this antenna system. Nearby transmit antennas can damage the receiver and the active antenna.
{: .callout-notice}

<!-- FLAG: Lightning WARNING pending. Was there lightning protection at K3LR? -->

#### Choose the site

The site must meet these conditions [DXE]:

- At least 4.6 m (15 ft) from power lines, buildings, towers, metal fences, other metal, and other antennas. More distance is better.
- Not on the same mast or tower as a transmit antenna.
- At least 1/2 wavelength from any transmit antenna, at the lowest frequency of that antenna.
- Soil where a ground rod can make a good ground. Where it cannot, you must add radials, or a ground screen over rock [DXE]. [ARC] says this applies to rocky or very dry soil. See [Check your work](#check-your-work).

#### Tools

From the manual [DXE]:

- Wrenches or nut drivers: 1/4 in, 5/16 in, 3/8 in, 7/16 in, 1/2 in
- Wrench: 5/8 in
- #2 Phillips screwdriver
- Allen wrenches: 7/64 in and 3/32 in (included in the kit)
- Knife or scissors, to cut weatherproofing tape

#### Parts

Parts in the kit are listed in the manual, Figure 3 [DXE]. The item numbers below are the manual's item numbers.

<!-- FLAG T-3: Replace the manual item numbers with BOM reference designators when the BOM exists. -->

Parts that are not in the kit [DXE]:

- Jet-Lube SS-30 (JTL-12555), for the element joints and all stainless steel hardware threads
- Loctite dielectric grease (LCT-37534), for the F connectors
- 3M Temflex tape (TES-2155), to weatherproof the F connectors
- 3M Super 88 vinyl electrical tape, as a UV overwrap
- Ground rod, 1/2 in to 3/4 in outside diameter, 4 ft to 6 ft long

<!-- FLAG: The manual gives two part numbers for the vinyl tape: TES-06143 (page 5) and TES-06132 (page 13). -->
<!-- FLAG: [ARC] specifies a 6 ft copper ground rod. [K3] used 1/2 in copper pipe driven 1.2 m (4 ft). Both fit the manual's range. Choose one for the BOM. -->

Parts for the separate DC power feed [ARC][K3]:

- 75 Ω RG-6 coax for RF. [DXE] recommends flooded quad-shield coax with compression F connectors.
- DC Power Cable
- F male power adapter, to connect the DC cable to the matching unit
- 12 V DC power supply
FLAG: Review F-SMA connection procedure

#### Prepare the work area

These tips come from the senior team's build [CAP]:

- Put a towel on the build surface. Small nuts can roll off and fall.
- Keep each part in its bag until you need it.
- Put loose hardware in resealable bags.
- Keep the shipping box. You can store the antenna in it.
- Move trash and unused parts away from the work area. Do not throw anything away until the end.
- Plan where the antenna will go after assembly. The assembled antenna is 2.59 m long.

#### About anti-seize

Anti-seize prevents galling on threads and joints and helps ensure correct torque [DXE]. The manual specifies Jet-Lube SS-30 for the joints between the antenna elements and for all stainless steel hardware threads [DXE].

You can use a generic anti-seize in place of SS-30.

Where to apply it:

- Stainless steel hardware threads: SS-30 or a generic anti-seize
- Joints between the aluminum antenna elements: a generic anti-seize only

> **NOTICE** Copper anti-seize on aluminum. Never put SS-30 on the aluminum antenna elements. SS-30 contains copper, which can cause galvanic corrosion on aluminum.
{: .callout-notice}

> **NOTICE** Anti-seize on connectors. Never put anti-seize on RF coax or power connectors.
{: .callout-notice}

### Set the power jumpers in the matching unit

The HFRx feeds DC power on a separate cable to keep noise off the RF coax [ARC]. You set this with jumpers J2 and J3 inside the matching unit (DXE-AVA-3).

1. Remove the cover from the matching unit.
2. Find the J1, J2, and J3 jumper headers. J2 and J3 are next to the F connectors.
3. Make sure that J1 is at the factory setting of -6 dB.

   The manual recommends -6 dB for the 2.6 m elements in this kit [DXE].

4. Move the J2 jumper from pins 1 and 2 to pins 2 and 3.
5. Move the J3 jumper from pins 1 and 2 to pins 2 and 3.

   Both J2 and J3 now connect pins 2 and 3. If only one jumper moved, the matching unit does not work [DXE].

6. Install the cover with the weep holes at the bottom.

<!-- PHOTO NEEDED (F-1): J2 and J3 at pins 2-3 -->

### Assemble the matching unit and clamps on the mounting plate

See Figure 1 and Figure 2 in the [DX Engineering DXE-RSEAV-1 manual (PDF, 1.5 MB, external site)](https://static.dxengineering.com/global/images/instructions/dxe-rseav-1fvi.pdf).

1. Turn the black mounting plate so the antenna mounting holes are near the top.
2. Put a flat washer on each of the two 1 in hex head bolts.
3. Put one bolt through the top hole of the matching unit and the mounting plate.
4. Put the other bolt through the bottom hole of the matching unit and the mounting plate.
5. Apply Jet-Lube SS-30 to the bolt threads.
6. Put a flat washer and then a split washer on each bolt.
7. Install a hex nut on each bolt.
8. Tighten the hex nuts.
9. Loosely install the two V-clamps (DXE-SSVC-1P) on the mounting plate.

   Each V-clamp has a U-bolt, a V-clamp, flat washers, split washers, and hex nuts. Keep the clamps loose so they can go over the ground rod later.

<!-- PHOTO NEEDED (F-1): matching unit on plate; V-clamps installed loosely -->

### Attach the bottom element to the mounting plate

See Figure 4, Figure 5, and Figure 6 in the [DX Engineering DXE-RSEAV-1 manual (PDF, 1.5 MB, external site)](https://static.dxengineering.com/global/images/instructions/dxe-rseav-1fvi.pdf).

The matching unit is already on the plate. Figure 5 shows this. You do not need to mount it again.

1. Put a #10 flat washer on a #10-24 × 1-1/2 in hex head cap screw.
2. Put the screw through the top element hole of the mounting plate, from the matching unit side.
3. Put a #10 flat washer and a #10-24 hex nut on the screw.
4. Tighten the hex nut.
5. Do steps 1 to 4 again with the second screw in the bottom element hole.
6. Put a #10 flat washer and a spacer on each screw.
7. Find the side of the bottom element (item 2, 1/2 in tube) with the larger holes.
8. Put the bottom element on the two screws, with the larger holes toward the plate.

   The spacers are now inside the element.

9. Put an external tooth washer on the bottom screw.
10. Put the ring terminal of the short antenna wire on the bottom screw.

    The wire points toward the matching unit. Figure 6 shows the direction.

11. Put a #10 flat washer and a #10-24 nylon lock nut on the bottom screw.
12. Put a #10 flat washer and a #10-24 nylon lock nut on the top screw.
13. Tighten both nylon lock nuts.
14. Put the fork terminal of the short wire on the ANTENNA terminal, between its two flat washers.
15. Tighten the ANTENNA terminal.

<!-- PHOTO NEEDED (F-1): element on spacers; short wire on ANTENNA terminal -->

### Install the ground rod and the ground clamp

See Figure 7 and Figure 9 in the [DX Engineering DXE-RSEAV-1 manual (PDF, 1.5 MB, external site)](https://static.dxengineering.com/global/images/instructions/dxe-rseav-1fvi.pdf).

1. Attach the ring terminal of the long wire to the tab on the ground clamp (DXE-SSVC-1PG).

   Use the hex head bolt, external tooth washer, flat washer, split washer, and hex nut. Figure 7 shows the order.

2. Drive the ground rod into the soil at the chosen site.

   Leave approximately 0.4 m of the rod above the ground.

3. Install the ground clamp on the rod, approximately 240 mm below the top of the rod.
4. Turn the clamp so the ground tab is in the position that the manual shows.
5. Tighten the clamp with its U-bolt, flat washers, split washers, and hex nuts.

<!-- PHOTO NEEDED (F-1): ground clamp on rod -->

### Mount the antenna on the ground rod

See Figure 10 in the [DX Engineering DXE-RSEAV-1 manual (PDF, 1.5 MB, external site)](https://static.dxengineering.com/global/images/instructions/dxe-rseav-1fvi.pdf).

1. Put the two loose V-clamps on the mounting plate around the ground rod.
2. Move the plate up or down until the top of the rod is not higher than the black mounting plate.

   A rod above the plate interferes with the active element [DXE].

3. Tighten the two V-clamps.
4. Put the fork terminal of the long wire on the GROUND terminal, between its two washers.
5. Tighten the GROUND wing nut by hand only.

   The plate is vertical, and the matching unit weep holes face down.

> **NOTICE** Ground connection. Never connect the GROUND terminal or radials to a metal structure. A connection to metal adds noise [DXE].
{: .callout-notice}

<!-- PHOTO NEEDED (F-1): assembly on rod with ground wire -->

### Install the middle and top elements

See Figure 11 in the [DX Engineering DXE-RSEAV-1 manual (PDF, 1.5 MB, external site)](https://static.dxengineering.com/global/images/instructions/dxe-rseav-1fvi.pdf).

1. Apply Jet-Lube SS-30 to the joint between the bottom and middle elements.
2. Put the middle element into the bottom element.
3. Align the screw holes.
4. Put a #6-32 × 3/4 in socket head cap screw through each hole pair.

   The screw head goes inside the larger hole and touches the inner element.

5. Put a #6 flat washer and a #6-32 nylon lock nut on each screw.
6. Tighten each screw with the included Allen wrench.
7. Apply Jet-Lube SS-30 to the joint between the middle and top elements.
8. Put the top element into the middle element.
9. Put a #4-40 × 1/2 in socket head cap screw  through each hole pair.
10. Put a #4 flat washer and a #4-40 nylon lock nut on each screw.
11. Tighten each screw with the included Allen wrench.
12. Install the black vinyl cap on the top element.

    The assembled element is 2.59 m long.

> **Tip** If you join the elements on a table, lay them flat. This helps align the screws with the holes [CAP].
{: .callout-tip}

<!-- PHOTO NEEDED (F-1): #6 joint; #4 joint and cap -->

### Connect the RF coax and the DC power

The upper F connector, 75 Ω OUTPUT, carries RF only. The lower F connector, OPTIONAL DC POWER, carries 12 V DC [DXE][K3].

1. Apply dielectric grease (LCT-37534) to the RF coax F connector.
2. Connect the RF coax to the 75 Ω OUTPUT connector.
3. Leave a small loop in the coax at the matching unit.

   The loop relieves stress on the connector [DXE].

4. Attach the coax to the ground rod below the mounting plate.
5. Connect the positive DC wire to the center pin of the F male power adapter.
6. Connect the negative DC wire to the shell of the adapter.
7. Apply dielectric grease to the adapter.
8. Connect the adapter to the OPTIONAL DC POWER connector.
9. Wrap both F connectors with Temflex tape (TES-2155).
10. Wrap vinyl electrical tape over the Temflex tape.
11. Bury the RF coax for some distance from the antenna, if you can.

    This decouples the coax from noise [DXE].

12. Connect the DC cable to the 12 V DC power supply.
13. Connect the RF coax to the receive chain. See Build Receiver.

<!-- FLAG: [ARC] block diagram shows a common mode choke between the antenna and the low-pass filter. [DXE] names the DXE-RXFC-75 choke as optional. Decide if the HFRx build includes a choke. -->
<!-- FLAG V-11: Change "Build Receiver" to a site-relative link when that part has a final heading. -->
<!-- PHOTO NEEDED (F-1): both F connectors connected and taped -->

### Check your work

1. Turn on the 12 V DC power supply.

   The green LED on the matching unit comes on. If the LED stays off, check the J2 and J3 jumpers and the voltage at the matching unit [DXE].

2. Measure the DC voltage at the matching unit end of the DC cable.

   The voltage is at least 11.5 V. If it is less than 11 V, look for a bad connection along the cable [DXE].

3. Tune the receiver to a steady AM or low-band signal that is not skywave.
4. Write down the signal level.
5. Connect a 4.6 m wire to the GROUND terminal.
6. Lay the wire in a straight line, away from the coax.

   The signal and noise levels do not change. If they change, improve the ground [DXE]:

   - Add a second ground rod a few feet away and connect it to the first.
   - If ground rods do not work at the site, add 4, 8, or 12 equally spaced radials, each 4.6 m to 6.1 m long.
   - Over rock, use a ground screen with a radius of at least the element height, and no more than 6.1 m.

7. Turn off the DC power.

   The green LED goes off, and there is very little or no signal. If the signal is almost the same with power on and off, the matching unit is not getting power, or the coax carries common-mode noise. A DXE-RXFC-75 choke can remove common-mode noise [DXE].

Next: install the computer software.

<!-- FLAG: Steps 3 to 7 need a working receiver and software. Decide if these checks move to Operation or Verification. -->

### Maintain the antenna

Do these checks at regular intervals [DXE]:

1. Make sure the weep holes at the bottom of the matching unit are clear.
2. Make sure the coax connections are still weatherproofed.

<!-- FLAG: No source gives a maintenance interval. -->
<!-- FLAG: A-4 life cycle: this part and the next may belong in Operation. -->

### Take the antenna apart for storage

These steps come from the senior team's build [CAP].

1. Remove the screws that join the bottom and middle elements.
2. Slide the middle element into the bottom element.
3. Remove the top element.
4. Put the top element in the shipping box, separate from the rest of the antenna.
5. Put all other parts in the shipping box.

> **Tip** Work over a towel. The senior team dropped small screws and nuts while taking the antenna apart [CAP].
{: .callout-tip}


### Computer Software

#### Setting up a new station

You have a USB stick and a small computer with a radio receiver attached. About an hour from now the machine will record and decode HF signals on its own. It sends nothing to the outside world until you have checked it and said so. Read the first section before you touch anything: it is the only part that needs preparation.

**This erases the computer's internal disk.** Everything on it goes, with no further warning once you boot from the stick. Use a machine you intend to dedicate to this.

#### 1 · Collect these first

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

#### And physically, before you begin

- A mini-PC with **16 GB of RAM or more** and an internal **NVMe** drive. The installer writes only to an NVMe drive.
- The **RX888 Mk2 receiver and the LBE-1421 GPS clock** plugged in and powered before the first boot. A magnetometer, a TS-1 time injector or a local GPS time server, if you have one, can plug in now too; the station finds them by itself. Anything missing does not stop the install; you can add it later.
- A USB stick of **16 GB or more**. It gets overwritten.
- A screen and keyboard on the machine, until the wizard finishes.
- A network: a cable to your router (the machine takes its address automatically), or a Wi-Fi network you join during setup. Sites with only IPv6 work too.

#### 2 · Get the image and write the stick

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

#### 3 · Install

#### Boot from the stick

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

#### Answer the wizard

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

#### 4 · Check it, then turn on uploads

**A new station starts with its site sink switch at off.** It records and decodes, but sends no spots or data to wsprnet, pskreporter.info, wsprdaemon.org or PSWS. Only its heartbeat, the five-minute health report, goes out. That way nothing leaves until you know the station hears well and reports the right callsign and grid.

#### Ask the station how it stands

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

#### 5 · Things that look wrong and are not

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

#### Turning remote access off and on

Remote access starts on. To change that, log in to the recorder and type:

```
smd remote off        turn it off; it stays off across reboots
smd remote on         turn it on again
smd remote status     show the state
```

Off stops the tunnel your fleet admin uses and changes nothing else: every upload keeps running. The status panel on the machine's screen shows which state holds.

#### Register for PSWS uploads

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

## Verification

_text_
