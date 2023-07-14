# Lily58

Lily58 is 6×4+5keys column-staggered split keyboard.

![Lily58_01](https://user-images.githubusercontent.com/6285554/50394214-72479880-079f-11e9-9d91-33fdbf1d7715.jpg)
![2018-12-24 17 39 58](https://user-images.githubusercontent.com/6285554/50394779-05360200-07a3-11e9-82b5-066fd8907ecf.png)
Keyboard Maintainer: [Naoki Katahira](https://github.com/kata0510/) [Twitter:@F_YUUCHI](https://twitter.com/F_YUUCHI)  
Hardware Supported: Lily58 PCB, ProMicro  
Hardware Availability: [PCB & Case Data](https://github.com/kata0510/Lily58)


# Flashing the firmware

Go to your ```qmk_firmware/keyboards``` folder and clone this repository
there. Rename the ```lily58``` folder to something else and rename the cloned
repo to ```lily58```

To flash the firmware, use the following

```
qmk flash -kb lily58 -km default
```

or

```
    make lily58:default
```

See the [build environment setup](https://docs.qmk.fm/#/getting_started_build_tools) and the [make instructions](https://docs.qmk.fm/#/getting_started_make_guide) for more information. Brand new to QMK? Start with our [Complete Newbs Guide](https://docs.qmk.fm/#/newbs).
