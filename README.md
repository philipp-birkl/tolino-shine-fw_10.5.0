# Tolino Shine Firmware 10.5.0 Rooted

## Introduction
Getting my hands on a used [Tolino Shine](https://mytolino.de/ch/tolino-shine/uebersicht/) e-Book reader i got curious about the internals. After some research I found that there have been successful attempts to root and adb the device as extensively documented by [@hecke] in multiple blog posts [[1](#hecke1), [2](#hecke2), [3](h#ecke3)]. Following his steps it was easy to update my device version 1.0.1 to 1.9.0.
However after connecting my Tolino to the internet I was greeted with a (pretty naggy) forced update screen blocking all fuctionality. That is when I decided to edit the actual firmware to not loose ADB & root access.

## Steps
1. Download the current firmware 10.5.0 from the [Tolino Website](https://mytolino.de/ch/software-updates/).
2. Extract the firmware.
3. Apply the `free-tolino-10.5.0.patch` file.
4. copy `su` & `adbd` to `./system/bin/`.
5. Zip the firmware back up.
6. Sign the firmware with the android test key .
7. Upload the firmware to the SD-card and reboot the Tolino.

## Attention
This will remove the tolino public key and replace it with the android test one. As I will give this device (modded) to a elderly relative I do not want them to accidentally update it via the Tolino update service and possibly locking us out again.

I recomend everyone attempting to do the same to read through [@hecke]'s blog posts!

**Why don't I update the test-key signed firmware?** Copyright. It contains copyrighted material I will not remove and I do not have the time or passion to deal with DCMA requests.

<b id="hecke1">[1]</b> hecke, '[collected: shiny ADB and root – the f*c**@! (:=easy) way](http://naberius.de/2013/06/26/collected-shiny-adb-and-root-the-fc-easy-way/)', 26-06-2013
<br/>
<b id="hecke2">[2]</b> hecke, '[collected: shiny new update keys for 1.2.4](http://naberius.de/2013/10/24/collected-shiny-new-update-keys-for-1-2-4/)', 24-10-2013
<br/>
<b id="hecke3">[3]</b> hecke, '[Tolino Shine – update 1.9.0 with adbd and testkeys](http://naberius.de/2017/02/26/tolino-shine-update-1-9-0-with-adbd-and-testkeys/)', 26-02-2017


[@hecke]: http://naberius.de/