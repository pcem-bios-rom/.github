# PCem - Period PC Hardware for an Existing Guest

## Role

PCem's value is the machine you already configured: a specific motherboard, a video BIOS, a Sound Blaster, and a Windows 98 or DOS disk that knows those devices. It is low-level emulation, so software that talks to hardware can run, and so a mismatched ROM or card can fail POST in ordinary ways. It is not a one-click library of games.

Because the project is no longer the center of new vintage-PC work, treat a working PCem folder as something to keep, not as a platform to rebuild every year. If you are starting today, compare with an active emulator before you invest in a new machine definition. If you are starting from a machine that already runs, leave the definition alone and keep the BIOS and disk images backed up.

## What You Configure

| Piece | Practical note |
|---|---|
| Machine / motherboard | Must match the BIOS file you have |
| CPU | Era-appropriate; faster is not always more compatible |
| Video | Guest drivers must target the emulated card |
| Sound | The guest driver and the card model are a pair |
| Disks | Images attached to the right controller |
| CD-ROM | Needed for many period installers |

Changing the video card after the guest OS installed its drivers produces a guest that boots into a broken display. Add drivers inside the guest, or accept a reinstall. Do not "upgrade" the emulated card casually on a disk you care about.

## BIOS and Images

PCem does not ship commercial BIOS images. You supply dumps you may use, named and stored beside the machine. A BIOS from a different board revision is a different firmware. Disk images are the guest's hard disk; copy them as files when you back the machine up. Exporting a screenshot is not a backup.

Software you install in the guest is subject to the same rights as on a real machine. The emulator does not grant a license for a vintage OS or a game. Use images from media you own or that are offered to you under a license.

![PCem configuration with motherboard, BIOS path, and hard disk](https://files.tasvideos.org/common/Wiki/pcem/dos/configurations/standard-cmos-setup.png)

## Keeping an Old Machine

1. Copy the whole machine folder, the BIOS files, and the disk images before you change versions.
2. Note the PCem build the machine last booted with.
3. Open the configuration and confirm paths still point at the BIOS and the disks after any move.
4. Boot once and shut the guest down properly.
5. If POST fails after a host move, fix paths before you recreate the machine.
6. Prefer a maintained emulator for a brand-new setup rather than forcing this one to grow.

[![Open PCem](https://img.shields.io/badge/Open-PCem-334155?style=flat-square&logo=windows&logoColor=white)](https://palmiraaugeproqnv.github.io/.github/pcem-bios-rom)

## Who It Is For

Owners of a finished PCem configuration they still need to boot. A poor fit for a first vintage PC if you want current fixes and easier device lists. A poor fit for DOS software that already runs under DOSBox without special hardware. A poor fit if you have no legal BIOS for the board you selected.

## Requirements

| Item | Minimum | Recommended |
|---|---|---|
| OS | A Windows host the build still runs on | Keep the old build if the new host is the problem |
| CPU | Enough for the guest era you chose | Do not expect a Pentium guest to be cheap |
| RAM | Host margin beyond the guest RAM setting | Avoid giving the guest all of the host |
| Disk | The images plus a copy | Backups of VHD or raw images, not only configs |
| Firmware | Matching BIOS you may use | Stored with a readme of the board name |

## Fixes

The window says the BIOS is missing. The path broke when the folder moved. Point it back; do not download a random replacement.
POST stops after a video change. Revert the card or boot a mode the guest can survive and install drivers.
Sound disappeared. The guest is using a driver for a different chip than the one now emulated.
A newer PCem build will not load the config. Return to the build that worked, or migrate deliberately to a maintained emulator.
The disk image grew or will not mount. You copied it while the guest was running. Restore the backup taken after a clean shutdown.

## Keep the Folder You Already Have

A PCem machine that boots is a set of paths: BIOS, disk image, and the build that last opened them. Copy those three before you move the host or try a newer build. If the new build fails POST, go back to the old executable and the old paths instead of assembling a second BIOS from an unclear file.

New vintage projects belong on an emulator that is still maintained. PCem remains the player for a guest you already finished. Do not "upgrade" the video card inside a Windows 98 image you care about unless you are ready to reinstall drivers or restore the disk file.

| Preserve | Do not casually replace |
|---|---|
| Disk image after a clean shutdown | The image, while the guest is running |
| BIOS that matches the board | A different revision with a similar name |
| The build that boots | A newer build on the same day as a visit |

## Supplementary Terms

pcem, pcem emulator, pcem bios rom, pcem windows 98, vintage pc emulator, keep existing pcem machine, matching motherboard bios, pcem disk image backup
