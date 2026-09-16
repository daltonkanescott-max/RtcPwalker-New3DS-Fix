# RtcPwalker New3DS Fix

Experimental compatibility improvements for **RtcPwalker** on New Nintendo 3DS-family systems, developed and tested primarily on a **New Nintendo 2DS XL**.

> **This is an unofficial community modification. It is not an official RtcPwalker release.**

## Credits

This project is based on **RtcPwalker**, created by **francesco265**.

**Original project:**
https://github.com/francesco265/RtcPwalker

Full credit for the original RtcPwalker implementation goes to francesco265 and the contributors credited in the original repository.

This project only modifies portions of the original implementation to improve the behavior I experienced when using RtcPwalker on New 3DS-family hardware.

## Why This Exists

RtcPwalker allows the Nintendo 3DS family to communicate with the original Pokémon Pokéwalker when playing Pokémon HeartGold or SoulSilver through TWiLight Menu++.

While testing RtcPwalker on my **New Nintendo 2DS XL**, I experienced several issues during Pokéwalker communication, including:

* Unreliable Pokéwalker communication
* Heavy slowdown during transfers
* Temporary freezing/pausing
* Graphical corruption of the Pokéwalker communication icon
* Other graphical timing glitches

After testing several configurations, I found a combination that significantly improved communication on my New 2DS XL.

## What This Fix Changes

The current experimental build includes:

* New 2DS XL-specific communication timing adjustments
* **POST40K + GAP30** timing configuration
* ARM7 interrupt-handling adjustment during Pokéwalker/RTCom communication
* Reduced graphical corruption during transfers
* No screen-darkening workaround

The original graphical corruption of the Pokéwalker icon has not occurred during my current testing.

Some temporary slowdown or pausing may still occur while communicating with the Pokéwalker.

## Tested Hardware

Currently tested on:

* **New Nintendo 2DS XL**

Additional testing is wanted for:

* New Nintendo 3DS
* New Nintendo 3DS XL
* Additional New Nintendo 2DS XL systems
* Different HeartGold/SoulSilver regions and revisions

If you test this, please open an Issue and include your console model, game version/region, and what happened during Pokéwalker communication.

## ⚠️ Experimental — Back Up Your Save

**BACK UP YOUR Pokémon HeartGold/SoulSilver save before testing this.**

During development I encountered one instance where the game appeared to fall back to an older save after using the PC and saving.

This has **not been consistently reproduced**, and I have not confirmed that RtcPwalker or this modification caused it.

Because of that, this release should currently be considered **experimental**.

The original RtcPwalker documentation also recommends disabling the patch when Pokéwalker functionality is not being used.

## Requirements

You still need the normal RtcPwalker setup and prerequisites.

Please read the original RtcPwalker documentation before installing this modification:

https://github.com/francesco265/RtcPwalker

This includes the required RTCom-enabled `TwlBg.cxi` setup.

## Installation

### 1. Back up your files

Back up:

* Your Pokémon HeartGold/SoulSilver `.sav`
* Your existing `usrcheat.dat`

Your existing cheat database is normally located at:

`SD:/_nds/TWiLightMenu/extras/usrcheat.dat`

### 2. Download the release

Download the latest release from the **Releases** section of this repository.

### 3. Install the cheat database

Copy the included:

`usrcheat.dat`

to:

`SD:/_nds/TWiLightMenu/extras/usrcheat.dat`

Replace the existing file if prompted.

**Make sure you backed up your original first.**

### 4. Enable the patch

Open TWiLight Menu++ and navigate to Pokémon HeartGold or SoulSilver.

Open the game's cheat menu.

Enable **only the RtcPwalker New3DS/New2DS XL patch**.

### 5. Start the game

Launch HeartGold/SoulSilver and enter the Pokéwalker menu.

Keep the Pokéwalker relatively close to and pointed toward the 3DS infrared transceiver during communication.

## Known Limitations

This is still experimental.

Known behavior includes:

* Temporary slowdown during Pokéwalker communication
* Occasional pauses during communication
* Some UI/frame-timing glitches may still occur
* Communication may require another attempt if it fails
* Save behavior is still being investigated

Normal gameplay outside Pokéwalker communication has not been extensively tested with the patch continuously enabled.

For now, I recommend enabling the patch when you need Pokéwalker functionality and disabling it afterward.

## Reporting Results

Testing from other systems would be extremely helpful.

When reporting results, please include:

**Console:**
New 3DS / New 3DS XL / New 2DS XL

**Game:**
HeartGold / SoulSilver

**Region:**
USA / EUR / JPN / etc.

**Pokéwalker detected:**
Yes / No

**Send Pokémon:**
Working / Failed

**Return Pokémon:**
Working / Failed

**Graphical glitches:**
Yes / No

**Slowdown or pauses:**
Yes / No

**Save issues:**
Yes / No

Please include any other details that might help reproduce the problem.

## Disclaimer

This project is experimental and provided without warranty.

Always maintain backups of your save data before testing modified software.

No Pokémon ROMs, copyrighted game files, or Nintendo firmware are distributed with this project.

## License

This project is a modification based on the GPL-3.0-licensed RtcPwalker project.

See the original RtcPwalker repository for the original project, source code, credits, and license:

https://github.com/francesco265/RtcPwalker
