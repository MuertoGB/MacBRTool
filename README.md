**Mac BootROM Tool by David R:**
-
MacBRTool is used to update targeted Mac BootROMs using Apples EFI ROM Updater in EFI mode. This makes it easy to add APFS support and update the system ROM without needing to manually flash the SPIROM IC, or boot an Operating System. Everything is done automatically from an EFI shell on a handy bootable memory stick.

Before flashing the BootROM it's recommended to remove the internal storage device otherwise 'startup.nsh' may not run. Please also ensure the device is plugged in.

☕ If you'd like to make a donation for my work, please [see here](https://www.buymeacoffee.com/Muerto). Cheers. ☕

---
**Before you start:**
-
I'm not responsible if you do something wrong, if you're here I expect you to know what you're doing. Where I do my utmost to verify all information to my best ability, I'm also not responsible for any mistakes my end either. As they say, sometimes shit happens.

If 'startup.nsh' does not run, you must manually find the USB filesystem, e.g. `fs7:`, then run it manually.

---
**Download:**
-
Current Version: `1.0.0` - (RD not set)\
See the [Changelog](CHANGELOG.md).\
Downloads can be acquired in the [releases](https://github.com/MuertoGB/MacBRTool/releases) section.

---
**Creating a USB disk:**
-
To begin, format a USB disk in ExFAT, FAT32, VFAT or HFS+ using a GPT or MBR partition table, then....

- Option A: Manually copy all MacBRTool.iso files to the formatted USB disk.
- Option B: Use a bootable USB creation tool (Such as Rufus) and select SMC_Tool.iso as the source file.

---
**Updating the BootROM:**
-
  1. Plug in your USB disk and power on the Mac whilst holding the `Option ⌥` key.
  2. Load into `MacBRTool` from the boot menu and let startup.nsh run.
  3. Type updatebr.nsh then press enter, the BootROM will then be updated (if necessary).
  4. The machine will power off automatically once completed.

---
**Compatible Systems:**
-
**iMac**
```
iMac10,1   Mac-F2268CC8
iMac11,1   Mac-F2238BAE
iMac11,2   Mac-F2238AC8
iMac12,1   Mac-942B59F58194171B
iMac13,1   Mac-FC02E91DDD3FA6A4
iMac14,1   Mac-031B6874CF7F642A
iMac14,2   Mac-27ADBB7B4CEE8E61
iMac14,3   Mac-77EB7D7DAF985301
iMac14,4   Mac-81E3E92DD6088272
iMac16,1   Mac-A369DDC4E67F1C45
iMac15,1   Mac-FA842E06C61E91C5
iMac16,2   Mac-FFE5EF870D7BA81A
iMac17,1   Mac-B809C3757DA9BB8D
iMac18,1   Mac-4B682C642B45593E
iMac18,3   Mac-BE088AF8C5EB4FA2
```
**MacBook**
```
MacBook6,1   Mac-F22CBAC8
MacBook7,1   Mac-F22CB9C8
MacBook8,1   Mac-BE0E8AC46FE800CC
MacBook9,1   Mac-9AE82516C7C6B903
MacBook10,1  Mac-EE2EBD4B90B839A8
```
**MacBook Air**
```
MacBookAir3,1   Mac-942452F5819B1C1B
MacBookAir4,1   Mac-742912EFDBEE19B3
MacBookAir5,1   Mac-2E6FAB96566FE58C
MacBookAir6,1   Mac-7DF21CB3ED6977E5
MacBookAir7,1   Mac-937CB26E2E02BB01
```
**MacBook Pro**
```
MacBookPro10,1   Mac-C3EC7CD22292981F
MacBookPro10,2   Mac-AFD8A9D944EA4843
MacBookPro11,1   Mac-189A3D4F975D5FFC
MacBookPro11,2   Mac-2BD1B31983FE1663
MacBookPro11,4   Mac-06F11F11946D27C5
MacBookPro12,1   Mac-E43C1C25D4880AD6
MacBookPro13,1   Mac-473D31EABEB93F9B
MacBookPro13,2   Mac-66E35819EE2D0D05
MacBookPro13,3   Mac-A5C67F76ED83108C
MacBookPro14,1   Mac-B4831CEBD52A0C4C
MacBookPro14,2   Mac-CAD6701F7CEA0921
```
---
**Shell Screen resolution:**
-
Use the `mode` command to display a list of supported screen modes, type the highest mode available e.g. `mode 160 47`, then press return.

---
**Licenses and acknowledgements:**
-
Startup manager icon by [KBuHT](https://macosicons.com/#/u/KBuHT) on macOSicons.

---