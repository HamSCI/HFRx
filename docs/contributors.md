---
layout: archive
title: Contributors
permalink: /contributors/
---

<div class="doc-layout">

<details class="sidebar archive-toc" markdown="1" open>
<summary class="sidebar-title" title="Contents"><span>Contents</span></summary>

* TOC
{:toc}

</details>

<div class="doc-content" markdown="1">

**Release:** draft · **Date:** 2026-11-10 · **Authors:** Santino Gregorovic, Jason Lai, Sanika Chaturvedi · **License:** to be decided (see R-3)

## Why was ___ done this way?

When a reviewer asks "Why was the documentation organized this way?" or "Why is this rule/formatting/statement important" or something of the sort, this page shall explain why.

This page sets the standards that the HFRx guide is built on and the rules that follow from them. Every rule names its basis - a clause in a published standard, or a team choice with the reason.

This page is for the creation of the About, Preparation, Materials, Build, and Operation sections. It could also be left for future contributors who will revise these sections

---

## Notes for senior project team

### Criteria for standards

<details markdown="1">
<summary>How many we need and where they are</summary>

#### 1. Standards count (project needs 9)
{:.no_toc}

This page cites 8 documentation standards plus Diátaxis. Diátaxis is a framework, not a standard, so do not count it.

| # | Standard | # | Standard |
|---|---|---|---|
| 1 | IEC/IEEE 82079-1:2019 | 5 | NIST SP 811 (2008) |
| 2 | ISO/IEC/IEEE 26514:2022 | 6 | ASD-STE100 Issue 9 |
| 3 | DIN SPEC 3105-1:2020 | 7 | WCAG 2.2 |
| 4 | ANSI Z535.6-2023 | 8 | IEC 60617 |

#### 2. Additional (content) standards from project plan
{:.no_toc}

These will be cited inside the steps they govern, not on this page. (Senior Project team choose one more to meet 9 criteria)

- **TOP CHOICE: NFPA 780-2026, Installation of Lightning Protection Systems**<br>Antenna section: grounding and surge protection. Lightning is the only WARNING-level hazard in the guide, so this one carries weight.
- **47 CFR Part 15, Radio Frequency Devices**<br>Build section: justifies DC-line chokes and linear supplies as required steps (RF noise degrades weak-signal reception).
- **IEC 62368-1:2023, Audio/video, information and communication technology equipment - Safety**<br>Build/Preparation: identifies where hazardous energy enters the station; feeds the safety messages written under ANSI Z535.6.
- **IEC 60529, Degrees of protection provided by enclosures (IP Code)**<br>Antenna section: gives the weatherproofing an IP rating target.
- **ISO/IEC/IEEE 26513:2017** (testing user documentation) and **ISO/IEC/IEEE 29119-1:2022** (test concepts) were in the plan but are now covered by rule R-6 and 82079-1 clause 6.3.3.

</details>

### Verification for AI's content

<details markdown="1">
<summary>How did Claude read and interpret the technical standards 2026-11-10</summary>

#### 3. Verification status of the rules below
{:.no_toc}

- **Read directly from the copies in the standards folder:** 82079-1, 26514, DIN SPEC 3105-1, NIST SP 811, ASD-STE100.
- **IEC 60617:** read from the symbol chart in the folder (`toaz.info-iec-60617-symbols-pr...pdf`). This is a third-party chart (2014) of selected symbols, not IEC's official database. It has earth/ground, bonding, coax, connectors, fuse, surge diverter, resistor, capacitor, inductor, diode, LED, transformer and "converter, general symbol". It has NO antenna symbol. Cite the official IEC 60617 database on the page, not the chart, and check any symbol the chart lacks (antenna, amplifier, filter) there.
- **WCAG 2.2:** w3.org/TR/WCAG22 could not be fetched from this session. Read instead: W3C "What's New in WCAG 2.2" (Recommendation since 2023-10-05; 4.1.1 Parsing removed) and the WebAIM WCAG 2 checklist (wording and thresholds for each criterion cited below).
- **Diataxis:** read diataxis.fr "Start here" and the full-site export (tutorials, how-to guides, reference, explanation, compass, workflow, complex hierarchies).
- **Not read directly (no copy in the folder):** ANSI Z535.6 - rules taken from ANSI's and Clarion Safety's published summaries; every Z535.6 rule here is also backed by 82079-1 7.11.

</details>

### Example of using a rule

<details markdown="1">
<summary>How a standard was used to build this documentation</summary>

#### 4. Contrast finding (rule V-3)
{:.no_toc}

Minima 2.5.1 defaults fail WCAG 1.4.3 on the `#fdfdfd` background: link color `#2a7ae2` = 4.15:1, grey text `#828282` = 3.78:1 (need 4.5:1).

Fix in `assets/css/style.scss` before the `@import`:

```scss
$brand-color: #1f62c1;   // (5.77:1)
$grey-color:  #6e6e6e;   // (5.01:1)
```

</details>

## Standards foundation

### Standards we follow

<details markdown="1">
<summary>The eight standards behind the guide and what each requires</summary>

These standards govern how the guide is written, structured, and presented. Standards that govern the station itself, such as lightning protection, are cited inside the steps they apply to.

| Standard | Governs | Rule it sets here |
|---|---|---|
| **IEC/IEEE 82079-1:2019** Preparation of information for use (instructions for use) of products | Instructions for any product: audience, content, structure, safety information, and testing | The audience is defined. Every procedure has preliminary information, numbered single-action steps, and completion information. Safety notes appear up front and warnings appear at the step. Non-authors review each section and real users test it. This is the base standard. The others refine it. |
| **ISO/IEC/IEEE 26514:2022** Design and development of information for users | Information for users of software. Applies to the Software and Operation parts. | Every topic has one information type: conceptual, instructional, reference, or troubleshooting. An information model is applied. Task titles are verb phrases and concept titles are noun phrases. Commands separate literal text from values the reader supplies. |
| **DIN SPEC 3105-1:2020** Open source hardware: requirements for technical documentation | What an open source hardware project must publish | The guide names its authors, license, and the hardware version it covers. Each release has a number and a date. Design files are published in their original editable format as well as an export. |
| **ANSI Z535.6-2023** Product safety information in product manuals, instructions, and other collateral materials | Safety messages in manuals | Fixed signal words (DANGER, WARNING, CAUTION, NOTICE), the safety alert symbol, and fixed message content: hazard, how to avoid it, consequence. |
| **NIST SP 811 (2008)** Guide for the use of the International System of Units | Writing numbers and units | A space goes between number and unit. Only SI symbols are used. Ranges and tolerances are written so no reader can misread them. |
| **ASD-STE100 Issue 9 (2025)** Simplified Technical English | Controlled language for technical writing | Procedure sentences are 20 words or fewer. Each step has one instruction in the imperative, in active voice. Each item has one term. We use the writing rules only, not the dictionary (see W-10). |
| **WCAG 2.2** Web Content Accessibility Guidelines (W3C Recommendation, 2023) | Accessibility of the web pages | Every page meets Level AA. In practice: text contrast of at least 4.5:1, alt text on every image, real heading structure, link text that names its destination, color never the only cue, and pages that still work at 200 % zoom and 320 px width. |
| **IEC 60617** Graphical symbols for diagrams (IEC online database) | Symbols in wiring, grounding and schematic diagrams | Diagrams use IEC 60617 symbols, such as earth (ground), coaxial pair and surge diverter, and reference designators match the bill of materials. 82079-1 clause 9.11.1 requires this standard. |

</details>

### The information model: Diátaxis

<details markdown="1">
<summary>Why Diátaxis, and how its four types map onto the standards</summary>

82079-1 (clause 8.3.2) requires the guide to apply an information model. It allows "using an existing information model, for example an open source information model." 26514 (clause 8.4) likewise says a model "may be … adopted from an open source or standard industry information model." Diátaxis is the open source model we adopt. It is a documentation framework, not a standard. It is the method we use to meet the standards' requirement for an information model.

Diátaxis sorts all documentation into four types by asking two questions, which it calls the compass:

1. Does the content inform **action** (what the reader does) or **cognition** (what the reader knows)?
2. Does it serve **acquisition** of skill (study) or **application** of skill (work)?

Each type maps onto the information types the two standards define:

| Diátaxis type | Compass answer | Reader's need | 82079-1 / 26514 information type | HFRx example |
|---|---|---|---|---|
| Tutorial | Action, study | "Teach me": a guided lesson | Instructional | A first practice build, if we write one |
| How-to guide | Action, work | "Help me do this task" | Instructional; troubleshooting | Assemble the receiver, Install the antenna |
| Reference | Cognition, work | "Give me the facts" | Reference; glossary | Bill of materials, Glossary |
| Explanation | Cognition, study | "Help me understand why" | Conceptual | What is a PSWS? |

Diátaxis says the boundaries matter most: "Crossing or blurring the boundaries described in the map is at the heart of a vast number of problems in documentation." That is why each part has exactly one type (rule S-1).

Diátaxis also says it does not require four top-level divisions. It asks that documentation describe the product as users experience it. Our sections follow the order of the work (About, Preparation, Materials, Build, Operation), and the four types apply to the parts inside each section.

Diátaxis is used by Canonical (Ubuntu), Django, NumPy, and Cloudflare. It is cited as [diataxis.fr](https://diataxis.fr/).

</details>

### Where to read the standards

<details markdown="1">
<summary>Which clauses we use, and where to get each standard</summary>

| Standard | Clauses this page uses | Access |
|---|---|---|
| IEC/IEEE 82079-1 | 5.3, 6.2.2, 6.3.3, 7.2.1, 7.4 to 7.6, 7.11, 7.12, 8.2, 8.3, 9.9 to 9.15 | IEEE Xplore through the CWRU library |
| ISO/IEC/IEEE 26514 | 8.3 to 8.11, 9.2, 9.5, 9.7 to 9.12, 9.14 | IEEE Xplore through the CWRU library |
| DIN SPEC 3105-1 | All (13 pages) | Free from DIN Media |
| ANSI Z535.6 | Signal words, safety alert symbol, message content | Paid; ANSI Webstore |
| NIST SP 811 | Check list for reviewing manuscripts; chapters 6, 7, 10.5 | [Free from NIST](https://www.nist.gov/pml/special-publication-811) |
| ASD-STE100 | Part 1, sections 1 to 9 (writing rules) | Free on request from [asd-ste100.org](https://www.asd-ste100.org/) |
| WCAG 2.2 | 1.1.1, 1.3.1, 1.3.2, 1.4.1, 1.4.3, 1.4.4, 1.4.10, 1.4.11, 1.4.12, 2.4.2, 2.4.4, 2.4.6, 2.4.7, 3.2.3, 3.2.6 | [Free from W3C](https://www.w3.org/TR/WCAG22/). Plain-language checklist from [WebAIM](https://webaim.org/standards/wcag/checklist) |
| IEC 60617 | Symbols used in our diagrams (table under rule F-8) | IEC online database (subscription) |
| Diátaxis | Start here; Tutorials; How-to guides; Reference; Explanation; Compass; Complex hierarchies | [Free at diataxis.fr](https://diataxis.fr/start-here/) |

</details>

## Rules

### How to read the basis column

<details markdown="1">
<summary>What Req, Rec, Model, Plan, Team, and Info mean</summary>

Every source in the basis column carries one label.

| Label | Meaning |
|---|---|
| **Req** | Required. The standard says *shall*, or the rule comes from a standard we adopted in full: a WCAG 2.2 Level A or AA criterion (our target is Level AA), an ASD-STE100 writing rule, or the NIST SP 811 check list. |
| **Rec** | Recommended. The standard says *should*, and we have chosen to make it mandatory. |
| **Model** | Diátaxis guidance. Diátaxis is our adopted information model, so its guidance is mandatory here. |
| **Plan** | A commitment in our submitted project plan. |
| **Team** | No standard sets this. It is our decision, and the reason is given. |
| **Info** | Informative text in a standard (a note) that supports a Team rule but does not require it. |

Standard names are shortened in the tables: 82079 (IEC/IEEE 82079-1), 26514, DIN (DIN SPEC 3105-1), Z535 (ANSI Z535.6), SP 811, STE (ASD-STE100), WCAG. For WCAG, the level of each criterion is shown in brackets.

</details>

### Audience and scope

<details markdown="1">
<summary>Who the guide is for and what it must cover</summary>

| # | Rule | Basis |
|---|---|---|
| A-1 | The About page states:<br>• who the guide is for<br>• the skills it assumes<br>• the tools the reader needs<br><br>Proposed audience: *an amateur radio operator or engineering student who can solder through-hole parts and run commands in a Linux terminal, with no prior SDR experience.* | Req: 82079 6.2.2<br>Req: DIN 3.7 (recipients) |
| A-2 | No step depends on information outside the guide, except public documents it links to. | Req: DIN 5.1<br>Plan: milestone M5 |
| A-3 | • Include what the reader needs to do the task, and nothing more.<br>• Repeat critical safety information wherever it is needed. | Req: 82079 5.3.3 (minimalism) |
| A-4 | The guide covers the station's whole life cycle:<br>• prepare<br>• build<br>• operate<br>• maintain<br>• take down | Req: 82079 5.3.2 (completeness)<br>Req: DIN 6 (life cycle) |

</details>

### Structure

<details markdown="1">
<summary>How pages, parts, and headings are organized</summary>

| # | Rule | Basis |
|---|---|---|
| S-1 | • Each H2 part on a section page is exactly one Diátaxis type: tutorial, how-to, reference, or explanation.<br>• If unsure, answer the two compass questions. | Req: 26514 8.3 (one information type per topic)<br>Model: Diátaxis compass |
| S-2 | Part titles:<br>• How-to: a verb phrase that says exactly what the reader will achieve ("Install the antenna")<br>• Reference: a noun phrase ("Bill of materials")<br>• Explanation: a noun phrase, which may start with "About" ("About the GPS clock") | Req: 26514 8.5, 8.6<br>Model: Diátaxis how-to guides, explanation |
| S-3 | • Keep reference data (part lists, specifications, settings) out of procedures.<br>• Keep background explanation out of both.<br>• Link between them instead. | Req: 26514 8.3<br>Rec: 82079 9.10.6<br>Model: Diátaxis ("keep explanation closely bounded") |
| S-4 | Reference parts:<br>• describe and only describe, with neutral facts<br>• follow a fixed pattern<br>• are ordered the way the hardware is built (for example, the bill of materials grouped by subsystem) | Model: Diátaxis reference ("describe and only describe", "respect the structure of the machinery")<br>Req: 26514 8.7 (same structure for like information) |
| S-5 | Headings:<br>• The page title is the only H1.<br>• Parts are H2, and sub-parts are H3.<br>• Never skip a level.<br>• Never use bold text as a fake heading. | Req: WCAG 1.3.1 (A), 2.4.6 (AA)<br>Rec: 82079 8.4.2.2 (no more than four levels) |
| S-6 | Contents lists use the exact heading text. The site builds its contents lists from the headings, so this holds automatically. | Req: 26514 9.10.5 |
| S-7 | Sections follow the order of the work: About, Preparation, Materials, Build, Operation. | Rec: 82079 8.3.3 (task and life-cycle order) |
| S-8 | • The About section has a Glossary.<br>• Each section links a term to the Glossary on first use. | Req: 26514 8.11<br>Req: 82079 7.5 |
| S-9 | Split a long task into smaller parts, with a short overview that shows how they connect. | Rec: 82079 8.3.4.3<br>Rec: 26514 8.6 |
| S-10 | A safety part comes before any hands-on work, in Preparation:<br>• Its heading signals importance ("Safety: read before you start").<br>• It opens with a sentence telling the reader to read it. | Req: 82079 7.11.2, 7.11.4, 9.15.1 |
| S-11 | Each section page opens with two or three sentences that say:<br>• what the page covers<br>• what the reader will have done by the end | Model: Diátaxis complex hierarchies (landing pages introduce, not just list)<br>Rec: 26514 8.6 (short overview) |
| S-12 | • Add a part only when there is content for it.<br>• Placeholder headings are allowed while drafting.<br>• No page is released with an empty part. | Model: Diátaxis workflow (do not create empty structures)<br>Team: placeholders help us plan, but an empty heading misleads a reader. |

</details>

### Procedures

<details markdown="1">
<summary>How to lay out steps a reader can follow alone</summary>

| # | Rule | Basis |
|---|---|---|
| P-1 | Every how-to part has three blocks:<br>• **Before you start**: purpose, prerequisites, tools and parts, and warnings for the whole procedure<br>• **Steps**: the actions<br>• **Check your work**: how to confirm success, and what comes next | Req: 82079 8.3.4<br>Req: 26514 8.6 |
| P-2 | • Number steps 1, 2, 3 in the order they are done.<br>• Restart numbering under each H3, so a step can be cited as "Wire the station, step 3". | Req: 82079 8.3.4.3<br>Req: 26514 9.12<br>Team (restart): lets reviewers point to a step. |
| P-3 | One action per step. If a step needs "and then", split it. | Req: 26514 8.6<br>Req: STE 5.2 |
| P-4 | Start each step with an imperative verb: Solder, Connect, Run, Measure. | Req: 26514 8.6<br>Req: STE 5.3 |
| P-5 | After any step whose result can be seen or measured:<br>• state the expected result<br>• write it on its own line, unnumbered<br>• say what to do if the result is wrong | Req: 82079 8.3.4.3<br>Rec: 26514 9.12 |
| P-6 | Put a condition before its action: "If the LED stays off, check J2." | Req: STE 5.4 |
| P-7 | Put a warning before the step it applies to, never after. | Req: 82079 7.11.5.1, 8.3.4.3 |
| P-8 | • Never hide a required step in a note, a caption, or a link.<br>• Notes give information, not instructions. | Req: STE 5.5<br>Team: a reader who skims skips notes and captions. |
| P-9 | Where the reader has a choice (for example, two antenna mounts):<br>• show both options<br>• show where each rejoins the main procedure | Rec: 82079 8.3.4.3 |
| P-10 | Each assembly step names:<br>• the parts involved<br>• their orientation<br>• the action<br>• the tool<br>• how to confirm the connection is correct | Req: 82079 7.12 (self-assembly products) |

</details>

### Writing

<details markdown="1">
<summary>Sentence length, voice, and word choice</summary>

| # | Rule | Basis |
|---|---|---|
| W-1 | Sentence length:<br>• procedure sentences: 20 words or fewer<br>• descriptive sentences: 25 words or fewer | Req: STE 5.1, 6.3<br>Rec: 82079 9.10.5 |
| W-2 | Use the active voice. | Req: STE 3.6 |
| W-3 | • No contractions.<br>• No dropped words such as "the". | Req: STE 4.2 |
| W-4 | Each paragraph has:<br>• one topic<br>• no more than six sentences | Req: STE 6.5, 6.6 |
| W-5 | • Use a vertical list for complex text.<br>• Split a list of more than about seven items into groups. | Req: STE 4.3<br>Model: Diátaxis complex hierarchies (about seven items is a comfortable limit) |
| W-6 | No semicolons. | Req: STE 8.1 |
| W-7 | • Address the reader as "you", in the present tense.<br>• Exception: a tutorial part may use "we" ("We will build a test antenna"). | Team: matches the imperative steps (P-4). The old documentation mixed "I" and "we".<br>Model (exception): Diátaxis tutorials use first-person plural. |
| W-8 | Never write "simply", "just", "easy", or "obviously". | Team: these words add no information, and they tell a struggling reader the problem is them. |
| W-9 | Use American English spelling. | Req: STE 1.14<br>Team: matches the HamSCI site. |
| W-10 | • Follow the STE writing rules.<br>• Do not adopt the STE dictionary of approved words. | Team: the dictionary is built for aerospace maintenance. Checking every word against it would cost more than our walkthroughs (R-6) gain from it. |

</details>

### Terminology

<details markdown="1">
<summary>Consistent names for parts, terms, and on-screen text</summary>

| # | Rule | Basis |
|---|---|---|
| T-1 | • One term per item, and one meaning per term.<br>• Choose "receiver" or "radio" and never switch. | Req: 82079 7.5<br>Req: STE 1.11 |
| T-2 | • Define in the Glossary every term the audience may not know.<br>• Spell out each acronym on its first use on each page. | Req: 82079 7.5, 7.6<br>Req: 26514 8.11 |
| T-3 | • Name parts exactly as the bill of materials does.<br>• Give the reference designator on first mention in a part: "10 µF capacitor (C3)". | Req: 82079 5.3.6 (consistency)<br>Team: lets every part trace to the procurement record (milestone M3). |
| T-4 | Write UI labels, file names, and commands exactly as they appear on screen, in code format: `config.ini`, **Save**. | Rec: 26514 9.8.1 |
| T-5 | The About page explains the guide's conventions once:<br>• code format<br>• `<placeholders>`<br>• signal words<br>• callouts | Req: 82079 7.4<br>Req: 26514 9.8.2 |
| T-6 | • Write "ground", not "earth", in text.<br>• Diagram symbols still follow IEC 60617. | Team: follows W-9 (American English). IEC 60617 lists "Ground (US)" as the name of the earth symbol. |

</details>

### Numbers and units

<details markdown="1">
<summary>How to write values, units, ranges, and dates</summary>

| # | Rule | Right | Wrong | Basis |
|---|---|---|---|---|
| U-1 | • Use SI units and units accepted for use with SI.<br>• Give other units in parentheses only where a part is sold that way. | 3 m (10 ft) coax | 10 ft coax | Req: SP 811 check list (1) |
| U-2 | • Put a space between number and unit symbol, even when the value is used as an adjective.<br>• Exception: angles in degrees. | 5 V, 10 MHz, 3.3 kΩ, 25 °C, a 25 kg mast, 45° | 5V, 25-kg mast | Req: SP 811 check list (10)<br>Req: SP 811 7.2 |
| U-3 | Use only standard symbols, in the correct case. | V, mA, kHz, MHz, kΩ, s | v, KHz, mhz, 3k3, sec | Req: SP 811 check list (2)<br>Req: SP 811 6.1.2, 6.1.8 |
| U-4 | Repeat the unit in every range and tolerance. | 4.9 V to 5.1 V; (1 to 30) MHz; (5.0 ± 0.1) V | 1–30 MHz; 5 ± 0.1 V | Req: SP 811 check list (7) |
| U-5 | Put a space before the percent sign. | 5 % | 5% | Req: SP 811 7.10.2 |
| U-6 | Do not mix unit names and symbols. | 3.3 kΩ or 3.3 kilohms | 3.3 k ohms | Req: SP 811 check list (8) |
| U-7 | Write values with units in numerals, not words. | 15 A | fifteen amps | Req: SP 811 check list (9) |
| U-8 | • Group digits in threes with a space when a number has more than four digits on either side of the decimal point.<br>• Choose the prefix that keeps numbers short.<br>• Values inside code and config files stay exactly as the software expects them. | 14 095.6 kHz | 14,095.6 kHz | Req: SP 811 check list (11)<br>Req: SP 811 7.9 |
| U-9 | Write dates as YYYY-MM-DD. | 2026-11-04 | 11/4/2026 | Team: a reader outside the US could read 11/4 as April 11. |

</details>

### Safety messages

<details markdown="1">
<summary>Signal words, the alert symbol, and where hazard warnings go</summary>

| # | Rule | Basis |
|---|---|---|
| SM-1 | Use only the four signal words below, chosen by the worst likely outcome. | Req: Z535<br>Rec: 82079 7.11.5.3, 7.11.5.4 |
| SM-2 | • Put the safety alert symbol (⚠) before DANGER, WARNING, and CAUTION.<br>• Never use it with NOTICE. | Req: Z535 |
| SM-3 | Write each message in this order:<br>1. the signal word<br>2. the hazard, in a few words<br>3. a command that says how to avoid it<br>4. what happens if the reader does not | Req: 82079 7.11.5.1, 7.11.5.2 (starts with the signal word)<br>Req: 26514 9.11<br>Req: STE 7.1 to 7.3 (command first, then the risk)<br>Req: Z535 |
| SM-4 | • Warnings for the whole procedure go in **Before you start**.<br>• A step-specific warning goes immediately before its step, even if it is also listed above. Readers can jump to a step straight from the sidebar. | Req: 82079 7.11.2, 7.11.5.1, 5.3.3 (repeat critical information) |
| SM-5 | Never use the word "Note" for a hazard. | Req: 26514 9.11 |
| SM-6 | List personal protective equipment at the start of any procedure that needs it. | Req: 82079 7.11.2 |
| SM-7 | A safety message stands out without color:<br>• signal word in bold capitals<br>• inside a bordered callout | Req: 82079 9.15.1<br>Req: WCAG 1.4.1 (A) |

| Signal word | Use when | HFRx examples |
|---|---|---|
| ⚠ DANGER | Will cause death or serious injury | Antenna near overhead power lines |
| ⚠ WARNING | Could cause death or serious injury | Lightning; mains wiring; work on a roof or ladder |
| ⚠ CAUTION | Could cause minor or moderate injury | Hot soldering iron; sharp coax-stripping tools |
| NOTICE | Could damage equipment or data, with no injury | ESD; reversed polarity; SD card corruption |

Example of SM-3:

> **⚠ WARNING** Lightning. Disconnect the coax from the receiver before a storm. A strike can travel along the coax and cause fire or electric shock.

</details>

### Visual and typographic standards

<details markdown="1">
<summary>Type, layout, contrast, and formatting on the site</summary>

The site uses the Minima 2.5 theme. These rules keep Minima's type and change only what the guide needs. Values match `assets/css/style.scss`.

| # | Rule | Basis |
|---|---|---|
| V-1 | • One typeface: Minima's system font stack. Code uses the monospace font.<br>• Body text and tables: 16 px, line height 1.5.<br>• Headings: H2 28 px bold, with a divider line above. H3 20 px bold.<br>• Sidebar and Contents lists: 14 px to 16 px. Inline code: 15 px.<br>• No web fonts. | Team: system fonts load instantly on a weak connection at the farm.<br>Info: 82079 9.10.1 note (line spacing of at least 120 %; 1.5 meets it) |
| V-2 | Layout:<br>• Frame: 1100 px wide.<br>• Sidebar column: 200 px. Contents column on this page and the Archive: 260 px.<br>• Below 800 px, the sidebar stacks above the text.<br><br>Pages must still work:<br>• at 320 px width with no sideways scrolling (wide tables may scroll)<br>• at 200 % zoom<br>• with enlarged text spacing | Team: layout values as built.<br>Req: WCAG 1.4.4, 1.4.10, 1.4.12 (AA) |
| V-3 | Minimum contrast against the background:<br>• normal text: 4.5:1<br>• large text (24 px, or 18.66 px bold): 3:1<br>• icons, borders, and focus outlines: 3:1 | Req: WCAG 1.4.3, 1.4.11 (AA)<br>Req: 26514 9.7.1 (text legible against its background) |
| V-4 | Color is never the only cue:<br>• Each callout carries its signal word as text.<br>• Links are always underlined, because links shown only by color need an extra cue. | Req: WCAG 1.4.1 (A)<br>Rec: 82079 9.13<br>Rec: 26514 9.7.1, 9.9 |
| V-5 | Safety colors (red, orange, yellow) are used only for safety callouts. | Req: 82079 9.11.1<br>Rec: 26514 9.9 |
| V-6 | Emphasis:<br>• Bold: sparingly, for UI labels and signal words.<br>• Italics: only for new terms and placeholder values.<br>• Underline: only for links.<br>• Never write whole sentences in capitals. | Req: 82079 9.10.1<br>Rec: 26514 9.7.1, 9.7.3 |
| V-7 | Callouts come in four kinds, set with a class on a blockquote:<br>• `.callout-danger` (DANGER, WARNING)<br>• `.callout-caution`<br>• `.callout-notice`<br>• `.callout-tip`<br><br>Never put more than two callouts in a row. More than that belongs in the steps. | Req: 82079 7.11.5.2 (limit to essentials)<br>Team: warnings lose force when stacked. |
| V-8 | Commands:<br>• Put them in fenced code blocks with a language tag.<br>• Leave out the `$` prompt.<br>• Put expected output in a separate block labelled "Output:".<br>• Write a value the reader must replace as `<like-this>`, with a note on where to find it. | Req: 26514 9.8.2 (separate literals from variables), 8.8 (how to recognize success)<br>Team (no prompt): commands copy and paste cleanly. |
| V-9 | Tables:<br>• Every table has a header row, with units in the header.<br>• Tables of the same kind use the same columns.<br>• Each table sits next to the text it supports. | Req: 82079 9.12<br>Req: 26514 8.7<br>Req: WCAG 1.3.1 (A) |
| V-10 | Links:<br>• Link text names the destination, never "click here".<br>• Links that leave the guide say so.<br>• Downloads give the file type and size: "(PDF, 2 MB)". | Req: 26514 9.10.4<br>Req: WCAG 2.4.4 (A) |
| V-11 | Links to other pages of the guide use site-relative paths. | Team: the site is served under `/HFRx`, and absolute links break on forks or a change of domain. |
| V-12 | Each section page prints legibly on Letter or A4 paper:<br>• header and sidebar hidden<br>• figures, tables, and callouts kept unbroken | Rec: 82079 9.5<br>Team: the deployment site may have no internet. |
| V-13 | Every page uses the same callouts, tables, figure style, and heading styles. | Req: 82079 9.9<br>Req: 26514 9.2 |
| V-14 | Every page has a unique title that says what it covers. | Req: WCAG 2.4.2 (A) |
| V-15 | The header links and sidebar list the pages in the same order on every page. | Req: WCAG 3.2.3 (AA)<br>Req: 82079 9.6 (navigation) |
| V-16 | The "report a problem" link (open a GitHub issue) appears in the same place on every page. | Req: WCAG 3.2.6 (A)<br>Req: 82079 6.5 (a method for receiving reader feedback) |
| V-17 | Every link, button, and Contents toggle shows a visible outline when reached with the keyboard. | Req: WCAG 2.4.7, 1.4.11 (AA) |
| V-18 | Page content reads in a logical order in the source, not only on screen: sidebar, then content. | Req: WCAG 1.3.2 (A) |

</details>

### Figures, photos and diagrams

<details markdown="1">
<summary>Photos, diagrams, alt text, and diagram symbols</summary>

| # | Rule | Basis |
|---|---|---|
| F-1 | • Any step that changes how the hardware looks gets a photo.<br>• A step that only runs a command does not. | Req: 82079 7.12 (one step at a time, illustrated)<br>Team (no photo for commands): a photo of a terminal adds nothing a code block does not. |
| F-2 | Place each figure right after its first mention, in the order of the steps. | Req: 82079 9.11.2<br>Rec: 26514 9.14.2 |
| F-3 | Each photo:<br>• shows one action<br>• is taken from the builder's point of view, on a plain background<br>• marks the focus with one arrow or circle<br>• is not overloaded with detail | Rec: 82079 9.11.2<br>Req: 82079 9.11.3 (avoid information overload) |
| F-4 | Captions and titles:<br>• Figure captions sit below the figure and start "Figure n.", numbered through the page.<br>• Table titles sit above the table.<br>• Every caption makes sense without the body text. | Rec: 82079 9.11.4<br>Rec: 26514 9.14.1(e) |
| F-5 | Alt text:<br>• says what the reader needs from the image: "C3 placed at the top left of the board, stripe toward the edge", not "photo of board"<br>• is empty (`alt=""`) for a purely decorative image | Req: WCAG 1.1.1 (A)<br>Req: 26514 9.5.3 |
| F-6 | A diagram that carries information not in the text gets a one-sentence summary under it. | Req: 26514 9.5.3<br>Req: WCAG 1.1.1 (A) |
| F-7 | Diagrams:<br>• Draw them in an editable tool (draw.io, Inkscape, KiCad).<br>• Export them as SVG.<br>• Commit the source file next to the export. | Req: DIN 5.3 (original editable format plus an export) |
| F-8 | • Diagrams use IEC 60617 symbols from the table below.<br>• Reference designators match the bill of materials.<br>• Block diagrams of whole modules (receiver, GPS clock, computer) may use labelled boxes. | Req: 82079 9.11.1<br>Team (designators): traces each symbol to a purchased part.<br>Team (boxes): our modules are bought complete, not built from components. |
| F-9 | • All diagrams share the same font, line weights, and arrowheads.<br>• Use shading only when it carries meaning. | Req: 26514 9.14.1 |
| F-10 | Image files:<br>• Photos: JPEG, 1600 px on the long edge, under 400 KB.<br>• Screenshots: PNG, cropped to the relevant window, personal data removed.<br>• File names: `<section>-<part>-<nn>.jpg`, in `assets/images/`.<br>• Images below the first screen use `loading="lazy"`. | Team: keeps pages fast on the farm's connection.<br>Info: 82079 9.11.2 (resolution below 72 dpi impedes clarity) |
| F-11 | Text inside a figure is no smaller than caption text at the displayed width. | Req: 26514 9.7.1<br>Req: 82079 9.10.1 |

IEC 60617 symbols the HFRx diagrams are expected to need:

| Use in HFRx | IEC 60617 symbol name |
|---|---|
| Antenna ground rod; station ground | Earth, general symbol (Ground, US) |
| Bonding the mast, enclosure and equipment together | Protective equipotential bonding (for safety bonds); functional equipotential bonding (for signal reference only). Use the one that matches the purpose. |
| Coax feed line | Coaxial pair; coaxial pair with screen |
| Lightning protection on the feed line | Surge diverter; lightning arrester |
| Plugs and jacks (SMA, BNC, power) | Contact, female (socket); contact, male (plug); plug and socket |
| Fuse on the DC supply | Fuse, general symbol |
| DC-line chokes and filter parts | Inductor; choke. Inductor with magnetic core (ferrite). Capacitor, general symbol. Resistor, general symbol |
| Power supply, signal converter | Converter, general symbol |
| Status LEDs | Light emitting diode (LED), general symbol |
| Antenna, amplifier, filter | Look up in the official IEC 60617 database before drawing. Our reference chart does not include these symbols. |

</details>

### Release and review

<details markdown="1">
<summary>Versioning, licensing, and checks before each release</summary>

| # | Rule | Basis |
|---|---|---|
| R-1 | Every page shows its:<br>• title<br>• release number<br>• date<br>• authors<br>• license | Req: 82079 7.2.1 (title, date of issue, revision)<br>Req: DIN 5.1, 5.2<br>Team (every page): readers often land on a page straight from a search. |
| R-2 | • Each release is a tagged GitHub release.<br>• Its notes name the HFRx hardware version it applies to. | Req: DIN 5.2<br>Plan: milestone M9 |
| R-3 | Release the documentation under an open license that meets the OSHWA definition (for example CC BY-SA 4.0) | Req: DIN 3.2, 3.3, 5.1 |
| R-4 | • Every part traces to the procurement record.<br>• Every command traces to the command log. | Req: 82079 5.3.4 (correctness)<br>Plan: milestones M3, M6 |
| R-5 | A team member who did not write a section checks it against these rules before it is pushed. | Rec: 82079 6.3.3 (editing by someone other than the writer) |
| R-6 | Before release:<br>• Someone outside the writing team who fits the audience (A-1) walks through each section.<br>• All defects are logged.<br>• Each defect is closed or listed as a known issue. | Rec: 82079 6.3.3 (walkthroughs, usability testing)<br>Plan: task 5.3, milestones M5, M9 |
| R-7 | When the hardware or software changes, review the affected pages before the next release. | Req: 82079 6.5 (keep information current across versions)<br>Rec: 82079 5.3.4 |

</details>

</div>
</div>
