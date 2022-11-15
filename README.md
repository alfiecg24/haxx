# haxx

This is a simple demo application I made to run the `weightBufs` kernel r/w exploit for all A12+ iOS devices on iOS 15.
Right now it supports T8020 (A12) on my iPad Air 3 - but you can amend it for other devices by going to the `_hwx_patch_model()` function inside `exploit.m`.
Change `mh->cpusubtype` to the CPU subtype of your device, this may take some trial and error.

The app has a console window to see the output of the exploit, and a button to run the exploit.
If you are debugging a crash/panic, then comment out `openConsolePipe()` in `ExploitView.swift` in order to have the output in Xcode console instead.

Original exploit can be found [here](https://github.com/0x36/weightBufs).

## To-do
* Improve exploit reliability on T8020
* Automatically assign cpuSubtype
