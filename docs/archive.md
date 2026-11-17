---
layout: archive
title: Archive
permalink: /archive/
mermaid: true
---

<div class="doc-layout">

<details class="sidebar archive-toc" markdown="1" open>
<summary class="sidebar-title" title="Contents"><span>Contents</span></summary>

* TOC
{:toc}

</details>

<div class="doc-content" markdown="1">

This page holds all the old (as of 2026-11-04) documentation.

# About
{% include archive/about.md %}

# Materials
{% include archive/materials.md %}

# Build
{% include archive/build.md %}

# Software
{% include archive/software.md %}

# Antenna
{% include archive/antenna.md %}

# Antenna Archive
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


# Data
{% include archive/data.md %}

</div>
</div>
