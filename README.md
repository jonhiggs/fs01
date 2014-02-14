TMK Footswitch
==============

This is a footswitch using TMK's keyboard firmware for a Teensy 2. As it's seen
by the OS as a keyboard it should work on any computer that supports USB
keyboards.

## 1. Ingredients

* 1 Normally open footswitch. I used an [M-GEAR sustain pedal](http://www.m-audio.com/products/en_us/SP2.html) for a keyboard.
* 1 [Teensy 2](http://www.pjrc.com/store/teensy.html)
* 1 Mini-USB cable long enough to run back to your computer.

## 2. Method
### 2.1 Hardware.
1. Disassemble your footswitch
2. Disconnect the original cable.
3. Remove any unnecessary switches and circuitry.
4. Connect the switch to B0 and B1 of your Teensy.
5. Fix your Teensy to the inside of your pedal.
6. Run your USB cable from the Teensy out of the pedal housing.

### 2.2. Environment
#### 2.2.1 OS X
1. `brew tap larsimmisch/avr`
2. `brew install avr-gcc`

### 2.3. Configuration

### 2.4. Building
1. Clone the TMK keyboard firmware from
[https://github.com/tmk/tmk_keyboard.git](https://github.com/tmk/tmk_keyboard.git)
2. `cd` into the checked out directory.
3. Add this repo as a submodule with `git submodule add
https://github.com/jonhiggs/fs01.git keyboards/fs01.git`
4. `make` the code.
5. Use the 'Teensy App' to program the hex file to your Teensy.
6. Enjoy your new footswitch.

