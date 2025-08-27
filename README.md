# MADCADDEN CUSTOM HARDDRV MAME

## WHAT IS MADCADDEN CUSTOM HARDDRV MAME?

This version of MAME is modified to play the Hard Drivin', Race Drivin', Race Drivin' Panorama, Street Drivin' and Hard Drivin's Airborne ROM's at a higher frame rate than regular MAME or the original arcade machine hardware. It comes pre-overclocked and has some custom features like a custom Dip Switch that lets you select between the standard MAME "Steering Wheel" and a "Custom Steering Wheel" which is calibrated better for Logitech G923 Steering Wheels so the steering is less twitchy. 

To calibrate the compact versions of Hard Drivin' and Race Drivin' you should select the "Calibration Wheel" and in the input settings you need to map "Calibration Wheel Analogue Inc" to the Kbd Right (right key on keyboard) and I recommend deleting the entry for "Calibration Wheel Analog". Once you do this you need to enter the test menu and start the steering calibration , it will tell you to turn the ignition key to start and once you do this hold down the left shift key on the keyboard and you will see a wheel value appear, it should say "1400". No whilst still holding the left shift key you need to hold down the right key you set earlier in the input menu to simulate the wheel turning 4 times. Now the following is important to get it set 100% accurately. As soon as you see the "wheel value" get to 2800 let go of the right key IMMEDIATLEY but keep the left shift button held down. You will see the wheel value slowly going back down to 1400 and as soon as it reaches 1400 press the ignition key! You should see a message saying "NEW CNTSPTRN 1024 PATCEN 0". If you see something like PATCEN -5 or something different it means you didn't let go of the right key quick enough when the wheel value reached 2800. Just do the calibration again and eventualy you should get it right. This is important to get the steering centered correctly on the compact versions of Hard Drivin' and Race Drivin'. After you have complete this you should enter the dip switch menu and switch the wheel back to "Steering Wheel" or "Custom Steering Wheel" if you are using a Logitech G923 wheel or similar. 

You DO NOT have to do this on the cockpit versions of the ROM's or the Race Drivin' Panorama / Hard Drvin's Airborne ROM's. To calibrate the steering in the cockpit versions and Race Drivin Panorama all you have to do is press the ignition key and dont touch the wheel and press it again to abort. This will automaticly calibrate the wheel to the correct values so all you have to do after that is calibrate the brake. You can skip the gear shifter calibration and the seat calibration as it's not needed for the game to work correctly.

I recommend playing the British version of Race Drivin' Panorama instead of Street Drivin' because it has the extra Stock Car track that Street Drivin' has and it has manual transmision cars which Street Drivin' is lacking. Street Drivin's audio is messed up too compared to Race Drivin's Panorama. The British version of Race Drivin' Panorama runs at a much higher frame rate but it doesn't have the multi monitor capabilities. If you want to play with multiple monitors use the official version of MAME instead but be aware the frame rate will be very low.


### How to compile?

If you're on a UNIX-like system (including Linux and macOS), it could be as easy as typing

```
make
```

for a full build, (usefull if you want to play other ROM's for other systems).




If you only want to play the Hard Drvin' / Race Drivin' series of Rom's then type this (it will compile much quicker).

```
make SUBTARGET=harddrv   SOURCES=src/mame/atari/harddriv.cpp,src/mame/atari/harddriv_m.cpp,src/mame/atari/harddriv_a.cpp,src/mame/atari/harddriv_v.cpp
```


See the [Compiling MAME](http://docs.mamedev.org/initialsetup/compilingmame.html) page on our documentation site for more information, including prerequisites for macOS and popular Linux distributions.

For recent versions of macOS you need to install [Xcode](https://developer.apple.com/xcode/) including command-line tools and [SDL 2.0](https://github.com/libsdl-org/SDL/releases/latest).

For Windows users, we provide a ready-made [build environment](http://www.mamedev.org/tools/) based on MinGW-w64.

Visual Studio builds are also possible, but you still need [build environment](http://www.mamedev.org/tools/) based on MinGW-w64.
In order to generate solution and project files just run:

```
make vs2022
```
or use this command to build it directly using msbuild

```
make vs2022 MSBUILD=1
```

### Coding standard

MAME source code should be viewed and edited with your editor set to use four spaces per tab. Tabs are used for initial indentation of lines, with one tab used per indentation level. Spaces are used for other alignment within a line.

Some parts of the code follow [Allman style](https://en.wikipedia.org/wiki/Indent_style#Allman_style); some parts of the code follow [K&R style](https://en.wikipedia.org/wiki/Indent_style#K.26R_style) -- mostly depending on who wrote the original version. **Above all else, be consistent with what you modify, and keep whitespace changes to a minimum when modifying existing source.** For new code, the majority tends to prefer Allman style, so if you don't care much, use that.

All contributors need to either add a standard header for license info (on new files) or inform us of their wishes regarding which of the following licenses they would like their code to be made available under: the [BSD-3-Clause](http://opensource.org/licenses/BSD-3-Clause) license, the [LGPL-2.1](http://opensource.org/licenses/LGPL-2.1), or the [GPL-2.0](http://opensource.org/licenses/GPL-2.0).

See more specific [C++ Coding Guidelines](https://docs.mamedev.org/contributing/cxx.html) on our documentation web site.

## License

The MAME project as a whole is made available under the terms of the
[GNU General Public License, version 2](http://opensource.org/licenses/GPL-2.0)
or later (GPL-2.0+), since it contains code made available under multiple
GPL-compatible licenses.  A great majority of the source files (over 90%
including core files) are made available under the terms of the
[3-clause BSD License](http://opensource.org/licenses/BSD-3-Clause), and we
would encourage new contributors to make their contributions available under the
terms of this license.

Please note that MAME is a registered trademark of Gregory Ember, and permission
is required to use the "MAME" name, logo, or wordmark.

<a href="http://opensource.org/licenses/GPL-2.0" target="_blank">
<img align="right" width="100" src="https://opensource.org/wp-content/uploads/2009/06/OSIApproved.svg">
</a>

    Copyright (c) 1997-2025  MAMEdev and contributors

    This program is free software; you can redistribute it and/or modify it
    under the terms of the GNU General Public License version 2, as provided in
    docs/legal/GPL-2.0.

    This program is distributed in the hope that it will be useful, but WITHOUT
    ANY WARRANTY; without even the implied warranty of MERCHANTABILITY or
    FITNESS FOR A PARTICULAR PURPOSE.  See the GNU General Public License for
    more details.

Please see [COPYING](COPYING) for more details.
