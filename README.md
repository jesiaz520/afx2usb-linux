axefx2-usb-setup
================

The `axefx2-usb-setup` program prepares your Linux system to load USB firmware
into an Axe-FX II connected via USB. You only need to run this program once on
each Linux system to which you'll connect your Axe-FX II.

Once your Linux system has been prepared, connecting an Axe-FX II via USB will
cause the USB firmware to be loaded into the Axe-FX II; this enables the
exchange of MIDI and audio signals between your Linux system and the Axe-FX II.

Your Linux system may require additional configuration to use the MIDI and
audio data. Such configuration is beyond the scope of this document.

Assuming that your Linux system uses ALSA for sound and MIDI, the following
commands may be used to quickly confirm a connection between your Linux sytem
and Axe-FX II:

```
$ amidi -l
$ aplay -l
$ arecord -l
```

In each case, the output should include a line that mentions `AXE-FX II`.

Prerequisites
-------------

* Linux 2.6.35 or later
* udev
* fxload

Acknowledgment
--------------

The `axefx2-usb-setup` program is based upon the work of Joachim Gahl. Joachim
did all the hard work of learning how to make Linux and an Axe-FX II
communicate. I merely simplified and reworked the script to meet my own
preferences and requirements.
