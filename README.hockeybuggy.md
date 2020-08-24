
# My QMK boards.

I have a few keyboards that use QMK (Quantum Mechanical Keyboard Firmware) and
I have a custom keymap for a few of them.


## Getting started

This repo is a fork of the QMK repo. To set things up we clone this repo, set
QMK as a remote called "upstream", then install dependencies.

```
git clone git@github.com:hockeybuggy/qmk_firmware.git
git remote add upstream git@github.com:qmk/qmk_firmware.git
./util/qmk_install.sh
```


## Maintaining this repo

To update my fork of the QMK repo:

```
git switch main
git pull origin main
git pull upstream master
git merge upstream/master
```


## Keyboards

### Preonic Rev2

Status: used daily

I started my own layout for this keyboard on my desktop a few years ago, but
didn't push the code somewhere before the desktop stopped booting.

```
# To build:
make preonic/rev2:hockeybuggy

# To build and flash:
make preonic/rev2:hockeybuggy:dfu
```


### Preonic Rev3

Status: often used

This keyboard is meant to be a "work" keyboard and my first Preonic to be a
"home" keyboard. Having two of the same keyboard was/is really nice in order to
not need to carry this keyboard around. (Note (2020/0823) I have unfortunately
not needed to take my keyboard elsewhere because of Covid related social
distancing.

```
# To build:
make preonic/rev3:hockeybuggy

# To build and flash:
make preonic/rev3:hockeybuggy:dfu
```


### ErgoDox Infinity

Status: Bad soldering in several switches

This was my first keyboard key. I find that it has more keys than I can keep in
my head. With so many physical keys I didn't really find a need to make use of
layers. I didn't like having my thumbs do different things, but at the time I
didn't create a keymap so I didn't change it.

```
make ergodox_infinity:defauilt
```
