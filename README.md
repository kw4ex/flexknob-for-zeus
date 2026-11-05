# FlexControl Knob for Zeus

Use the **FlexRadio FlexControl** USB tuning knob with **Zeus**, the SDR program for ANAN and other openHPSDR radios. Turning tunes VFO A with Zeus's step; a press can switch the knob to AF volume, AGC gain, VFO B, RIT, XIT, tuning step or TX drive; twelve presses (the knob press and buttons 1 to 3, each as tap, double tap or long press) each run a function you choose. Written for operators, not programmers: you download one file and Zeus installs it.

Version 1.0.1 (latest). Older versions stay on the Releases page.

## Download

**Start at the [Releases page](https://github.com/kw4ex/flexknob-for-zeus/releases).** The top entry marked **Latest** is the newest version; older versions are listed below it, each with its own files.

How to download (no GitHub account needed):

1. On the Releases page, click the version you want (the newest is at the top).
2. Scroll to the **Assets** list at the bottom. If you only see a few files, click **Show all … assets**.
3. Click the file for **your computer** (table below). Your browser saves it, normally in your **Downloads** folder.
4. **Don't click "Source code (zip)" or "Source code (tar.gz)"** - those are for programmers. **Don't unzip** the file; Zeus opens the `.zip` itself.
5. In Zeus: **Features > Community > Install local feature**, pick the `.zip`, then restart Zeus.
6. Add the panel: **Add Panel > Controls > FlexControl Knob**. Plug the knob into the computer that runs Zeus.

| Your computer | File name ends in |
| --- | --- |
| Windows PC | `-<version>.zip` (no extra word) |
| Mac with Apple silicon (M1-M4) | `-osx-arm64.zip` |
| Intel Mac | `-osx-x64.zip` |
| Linux PC (64-bit) | `-linux-x64.zip` |
| Raspberry Pi 4/5 (64-bit OS) | `-linux-arm64.zip` |

Not sure which Mac you have? Apple menu > **About This Mac**: "Chip: Apple M..." is Apple silicon, "Processor: Intel" is Intel.

To go back to an older version, scroll down the Releases page to it and download it the same way. Installing a version replaces the one you have.

## Instructions

- [Step-by-step guide (PDF)](docs/guides/FlexControl-Knob-for-Zeus-guide.pdf)
- Short reference: [src/FlexKnob/README.md](src/FlexKnob/README.md)

Only one program can open the knob at a time: close any other program that uses it (for example the KPA1500 Thetis bridge) while Zeus is running.

## Also by KW4EX

- [Elecraft KPA1500 for Zeus](https://github.com/kw4ex/kpa1500-for-zeus): meters and controls for the KPA1500 amplifier.
- [All of my Zeus and Thetis add-ons](https://github.com/kw4ex)

## No warranty - use at your own risk

This add-on is shared by one radio operator, **as is**. There is **no warranty of any kind**: no promise that it works, that it is safe, or that it suits your equipment or purpose. Radios, amplifiers and antennas can be damaged, and RF can be dangerous. You are responsible for checking that it behaves correctly with your own station, and for operating within your license. The author is not liable for any damage or loss. It is not made, approved or supported by FlexRadio, Elecraft or the Zeus project.

## For programmers

Build everything with `BUILD-FlexKnob.bat` (Windows) or `BUILD-FlexKnob-mac.command` (Mac), or `dotnet build Zeus.FlexKnob.slnx -c Release`. Tests: `dotnet run --project tests/FlexKnob.Tests -c Release`. Licence: GPL-2.0-or-later.
