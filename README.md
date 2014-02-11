TMK Footswitch
==============

This is a footswitch using TMK's keyboard firmware for a Teensy 2.

## 1. Ingredients

* 1 Normally open footswitch. I used an [M-GEAR sustain pedal](http://www.m-audio.com/products/en_us/SP2.html) for a keyboard.
* 1 [Teensy 2](http://www.pjrc.com/store/teensy.html)
* 1 Mini-USB cable long enough to run back to your computer.

## 2. Method

1. Disassemble your footswitch
2. Disconnect the original cable.
3. Remove any unnecessary switches and circuitry.
4. Connect the switch to B0 and B1 of your Teensy.
5. Fix your Teensy to the inside of your pedal.
6. Run your USB cable from the Teensy out of the pedal housing.
7. Clone the TMK keyboard firmware from https://github.com/tmk/tmk_keyboard.git
8. `cd` into the checked out directory.
9. Add this repo as a submodule with `git submodule add
https://github.com/jonhiggs/fs01.git keyboards/fs01.git`
10. `make` the code.
11. Use the 'Teensy App' to program the hex file to your Teensy.
12. Enjoy your new footswitch.

## 3. Notes

By default the switch sends `L_GUI` which on OS X is the `Command` key. You can
change the key that is sent in `keymap_plain.c`.
