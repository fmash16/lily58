# Lily58

Lily58 is 6×4+5keys column-staggered split keyboard.

![Lily58_01](https://user-images.githubusercontent.com/6285554/50394214-72479880-079f-11e9-9d91-33fdbf1d7715.jpg)
![2018-12-24 17 39 58](https://user-images.githubusercontent.com/6285554/50394779-05360200-07a3-11e9-82b5-066fd8907ecf.png)
Keyboard Maintainer: [Naoki Katahira](https://github.com/kata0510/) [Twitter:@F_YUUCHI](https://twitter.com/F_YUUCHI)  
Hardware Supported: Lily58 PCB, ProMicro  
Hardware Availability: [PCB & Case Data](https://github.com/kata0510/Lily58)

Make example for this keyboard (after setting up your build environment):

    make lily58:default

See the [build environment setup](https://docs.qmk.fm/#/getting_started_build_tools) and the [make instructions](https://docs.qmk.fm/#/getting_started_make_guide) for more information. Brand new to QMK? Start with our [Complete Newbs Guide](https://docs.qmk.fm/#/newbs).

# With encoder and underglow rgb

## macOS

- Install [Homebrew](https://brew.sh/)
- Install `qmk` with Homebrew

```sh
brew install qmk/qmk/qmk
```
- Clone `qmk_firmware` with submodules

```sh
git clone --recurse-submodules git@github.com:qmk/qmk_firmware.git
```

> Not cloning manually might result in error

- Run `qmk setup` to install the necessary dependencies

Now simply flash your profile with `qmk flash -kb lily58 -km <profile-name>`

## Windows

Install and setup QMK MSYS on your computer. After opening up the QMK MSYS
terminal, follow [this guide](https://msys.qmk.fm/guide.html) to setup qmk.

Now, once qmk is setup and ready to go, head over to keyboards directory
with

```sh
cd qmk_firmware/keyboards/
```

Here we have our default lily58 keyboard folder. We are going to remove it and
replace with this lily58 repository. To remove the default and make it
a backup, run the following

```sh
mv lily58 lily58.bak
```

Then, we clone into our lily58 repo

```sh
git clone https://github.com/fmash16/lily58
```

And that's it. Now you can run the following to flash your lily

```sh
qmk flash -kb lily58 -km fmash
```

Here we are flashing the fmash keymap, the default keymap does not have the
encoder functions set up. In order to edit or make your own keymap, you can
copy the fmash keymap, remap it to your name and work in there. The keymaps are
located in the ```~/qmk_firmware/keyboards/lily58/keymaps``` folder. 
So to make your own, you can run the following in order

```sh
cp -rv ~/qmk_firmware/keyboards/lily58/keymaps/fmash ~/qmk_firmware/keyboards/lily58/keymaps/{Your Name}
cd ~/qmk_firmware/keyboards/lily58/keymaps/{Your Name}
```

There, you can edit the keymap.c file to change your keymap and encoder
functions to your liking using notepad or any editor of your choice. 
To open with notepad:

```sh
notepad.exe keymap.c
```

Please head over to the qmk docs to get a guide on the configuration options.


If your are not comfortable in terminal, you can also navigate to your home folder on
windows e.g. ```C:/Users/username/```, The qmk_firmware folder is located there.
From there you can navigate to ```qmk_firmware/keyboards/lily58/keymaps``` to
find different keymaps. To make your own, create a folder in your own name and
copy the contents of the folder ```fmash``` into the new folder. There you can
edit the keymap.c file to change the keymap. The keycodes can be found at [qmk
docs](https://github.com/qmk/qmk_firmware/blob/master/docs/keycodes.md)
