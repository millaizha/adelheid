# 𝕬𝖉𝖊𝖑𝖍𝖊𝖎𝖉 Revision 1.0 (Superseeded by Revision 2.0)

**Disclaimer:** Revision 1.0 uses pin 37 (F6) for LED backlight. This causes the LEDs to flicker slightly because that pin is not a PWM pin.  
In Revision 2.0 the backlight and col4 pins are swapped. The new backlight pin is therefore pin 31 (C6) and col4 is on pin 37 (F6).  
Fortunately you can easily make a Revision 1.0 PCB compatible with the Revision 2.0 firmware so you can enjoy a steady LED backlight.  
The process is documented here &rarr; [REVISION-UPGRADE-INSTRUCTIONS.md](./REVISION-UPGRADE-INSTRUCTIONS.md)

The Adelheid is a 75% Alice-like keyboard.  
It's a fork of FateNozomi's Arisu files: [Arisu PCB](https://github.com/FateNozomi/arisu-pcb) &amp; [Arisu case](https://github.com/FateNozomi/arisu-case)

![adelheid](https://gist.githubusercontent.com/floookay/7bf6511a8d84804d32de4d7bbe3bd0fb/raw/559336bcb5f8c04bbea9ad8aab7397812ab72859/adelheid.jpg)
<!-- ![adelheid side](https://gist.githubusercontent.com/floookay/7bf6511a8d84804d32de4d7bbe3bd0fb/raw/4545813142abf2e65902b7caca10f7a3b39ebaed/side_shadow.jpg) -->

This repository includes files for:

- the Adelheid PCB &rarr; [README.md](./pcb/README.md)
- a layered case &rarr; [README.md](./case/README.md)
- a wrist rest &rarr; [README.md](./wrist-rest/README.md)

## Changes in this fork

Here is a list of things I added in this fork in comparison to the Arisu:

- [x] added an angled &amp; spaced function row
- [x] added option for stepped caps lock
- [x] replaced micro usb port with tht mini usb port
- [x] added single color underglow and key lighting **(WIP - underglow works, but per key LEDs have not been tested yet)**

for a visual comparison see [here](./IMAGES.md#arisu-comparison)

## Layout

A spaced 75% layout on top of the Alice/Arisu-layout.

[Keyboard-Layout-Editor](http://www.keyboard-layout-editor.com/#/gists/4262535adb5ac81a913edbebc4de8226) [(raw)](https://gist.github.com/floookay/4262535adb5ac81a913edbebc4de8226)  
![adelheid layout](https://gist.githubusercontent.com/floookay/7bf6511a8d84804d32de4d7bbe3bd0fb/raw/4545813142abf2e65902b7caca10f7a3b39ebaed/layout.png)  
<!-- ![adelheid top view](https://gist.githubusercontent.com/floookay/7bf6511a8d84804d32de4d7bbe3bd0fb/raw/4545813142abf2e65902b7caca10f7a3b39ebaed/top_view.jpg) -->

## Firmware

The firmware of Revision 1.0 and Revision 2.0 are incompatible because pins had to be swapped. The latest QMK firmware files for Revision 1.0 can be found under [this commit](https://github.com/floookay/qmk_firmware/commit/509ece8587e4c4dd17ae6ce7aae5302aec95cbb8).  
If you already have the files for Revision 2.0 but own a Revision 1.0 PCB consider manually upgrading your PCB to Revision 2.0 ([instructions](./REVISION-UPGRADE-INSTRUCTIONS.md)) so backlighting is properly supported, or (if you don't care about backlighting) edit the matrix and backlight pins in the firmware files.

For **Revision 1.0** the corresponding section in `config.h` should look like this:

```cpp
#define MATRIX_ROW_PINS { D0, F4, D1, D2, D3, D5, F7 }
#define MATRIX_COL_PINS { F0, F1, E6, C7, C6, B6, D4, B1, B0, B7, B5, B4, D7, D6, B3 }  // C6 instead of F6
…
#define BACKLIGHT_PIN F6    // F6 instead of C6
#define BACKLIGHT_LEVELS 3
```

## Images

For more images see [images.md](./IMAGES.md).

## Miscellaneous

> Why?

I think accessing the function keys with a layer on the number row is the superior method as it's faster and more comfortable because you barely have to move your hands. I found myself trying to access the function row one-handedly quite often and nothing beats the comfort of pressing a single dedicated key. By default you can still access the function keys via the number row on the secondary layer.

> Where does the name Adelheid come from?

I thought it'd be nice to continue the somewhat tradition of naming Alice-clones by putting a spin on the forename Alice, just like the Arisu, Lisa and Majbritt did. I chose Adelheid as a German spin on the name.  
The typeface is called Fraktur and was the dominant typeface during the time when Adelheid was one of the most popular names.

> Will you add more keys to the bottom row or a second B key?

I don't plan on changing the bottom row or adding a second B key. In my opinion the keyboard looks the best and most balanced the way Fate designed it.

## TODO's

- **test lighting support**
- add 3d printable case files
