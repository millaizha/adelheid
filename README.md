# 𝕬𝖉𝖊𝖑𝖍𝖊𝖎𝖉 - WIP

The Adelheid is a 75% Alice-like keyboard.  
It's a fork of FateNozomi's Arisu files: [Arisu PCB](https://github.com/FateNozomi/arisu-pcb) &amp; [Arisu case](https://github.com/FateNozomi/arisu-case)

![adelheid](./images/adelheid.png)

## Changes

- [x] added an angled spaced function row
- [x] added option for stepped caps lock
- [x] replaced micro usb port with tht mini usb port
- [ ] option for 2u backspace
- [ ] optional single color through hole led backlight &amp; SMD underglow?

## Layout

A spaced 75% layout on top of the Alice/Arisu-layout.

[Keyboard-Layout-Editor](http://www.keyboard-layout-editor.com/#/gists/4262535adb5ac81a913edbebc4de8226) [(raw)](https://gist.github.com/floookay/4262535adb5ac81a913edbebc4de8226)  
![adelheid_layout](./images/layout.png)  

## Firmware

<https://github.com/floookay/qmk_firmware/tree/adelheid/keyboards/adelheid>  
And hopefully soon in the main QMK repository.

## Miscellancious

> Why?

Good question, I think accessing the function keys with a layer on the number row is the superior method as it's faster and more comfortable because you don't have to move your hands. But I found myself trying to access the function row one-handedly quite often and nothing beats the comfort of pressing a dedicated key. So that's why I added a the function row. By default you can still access the function keys via the number row on the secondary layer.

> Where does the name Adelheid come from?

I thought it be nice to continue the somewhat tradition of naming Alice-clones by putting a spin on the forename Alice, just like the Arisu, Lisa and Majbritt did. I chose Adelheid as a German spin on the name since that's where I'm from.  
The typeface is called Fraktur and was the dominant typeface during the time when Adelheid was one of the most popular names.

> Are you planning on adding a 2u backspace?

Yes, I'll probably add that option to the PCB and case files in the coming weeks.

> I want RGB lighting, will you add RGB LED support to the PCB?

No, I won't add footprints for RGB LEDs. I think backlighting for many keysets looks best either off or in a single color. From experience I noticed that even if you have the possibility to change the colors on the go, you do it once and then never again. So I might add per key single color through hole LED support and SMD underglow.  
You could of course buy an RGB strip and use one of the free exposed pins to control the strip.

> Will you add more keys to the bottom row or a second B key?

I don't plan on changing the bottom row or adding a second B key. In my opinion the keyboard looks the best and most balanced the way Fate designed it.
