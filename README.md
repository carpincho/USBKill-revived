![usbkill](Resources/USBKillBanner.gif)
« usbkill-revived » is a repository that aims to add bug fixes and fix issues with the original USBKill project after its abandonment by its owner. It is fully FOSS, with the GNU General License.
To run:

```shell
sudo python usbkill.py
```
or
```shell
sudo python3 usbkill.py
```

Related project; same idea, but implemented as a Linux driver: https://github.com/NateBrune/silk-guardian (Unlike the original USBKill, this is actually still maintained.)


### Why?

Some reasons to use this tool:

- In case the police or other thugs come busting in (or steal your laptop from you when you are at a public library, as happened to Ross Ulbricht). The police commonly use a « [mouse jiggler](https://en.wikipedia.org/wiki/Mouse_jiggler) » to keep the screensaver and sleep mode from activating. Use this tool if you are an activist or otherwise need protection.
- You don’t want someone to add or copy documents to or from your computer via USB.
- You want to improve the security of your (encrypted) home or corporate server (e.g. Your Raspberry Pi).

> **[!] Important**: Make sure to use disk encryption for all folders that contain information you want to be private. Otherwise, they will get it anyway. Full disk encryption is the easiest and surest option if available

> **Tip**: Additionally, you may use a cord to attach a USB key to your wrist. Then insert the key into your computer and start usbkill. If they steal your laptop, the USB will be removed and the computer shuts down immediately.

### CHANGE LOG
(The usbkill-revived project uses the most recent version of USBKill before its abandonment. This will be a change log rather than a feature list. USBKill-Revived is updated every day or every other day. The changelog may be changed as new spontaneous bug fixes come in. For old changelogs, look at the README history.)

**(Version 1.1)**
-Issue #102 on the original USBKill repo has been fixed.

-The previous commands used to wipe SWAP were insufficient. There are now 3 commented presets that the user can use in lieu of the poor implementation of both the original USBKill swap eraser and the previous fix in Version 1.0. The user can either choose overwriting with /dev/urandom with ``dd``, use ``shred``, or wipe the swap with a random AES-256-CTR key, then wiping with /dev/zero as an overkill preset. 

**(TODO: Fix all other issues on the original repository.)**



### Supported command line arguments (partially for devs):

- -h or --help: show help message, exit.
- --version: show version of the program, exit.
- --no-shut-down: if a malicious change on the USB ports is detected, execute all the (destructive) commands you defined in settings.ini, but don’t turn off the computer.
- --cs: Copy program folder settings.ini to /etc/usbkill/settings.ini

### Contact
The contact for the maintainer of the usbkill-revived aka me is wobsterious@proton.me 

If you need the owner's email for some reason (it's abandoned) then it is available on the official USBKill project repository.

