<h1 align="center">
<img width="200" src="resource/img/icon256.png" alt="SMCFT Logo">
<br>
Mac BootROM Tool
</h1>

<h4 align="center">Making BootROM flashing quicker and easier.</h4>

<p align="center">
  <a href="#about">About</a> •
  <a href="#download">Download</a> •
  <a href="#bootable-usb">Bootable USB</a> •
  <a href="#updating-the-bootrom">Updating the BootROM</a> •
  <a href="#compatibility">Compatibility</a> •
  <a href="#disclaimers">Disclaimers</a> •
  <a href="#acknowledgements">Acknowledgements</a> •
  <a href="#donate">Donate</a>
</p>

## About

MacBRTool is used to update targeted Mac BootROMs using Apples EFI ROM Updater in EFI mode. This makes it easy to add APFS support and update the system ROM without needing to manually flash the SPIROM IC, or boot an Operating System. Everything is done automatically from an EFI shell on a handy bootable memory stick.

## Download

| Version| Release Date| Latest|
|--------|-------------|--------|
|[V1.0.1](https://github.com/MuertoGB/MacBRTool/releases/tag/v1.0.1)|not Set |`Yes`|
|[V1.0.0](https://github.com/MuertoGB/MacBRTool/releases/tag/v1.0.0)|2nd Feb 2023|`No` |

> 📔 See the full [Changelog](CHANGELOG.md).

## Bootable USB

To begin, format a USB disk in ExFAT, FAT32, VFAT or HFS+ for use with MacBRTool.
> ⚠ FAT32 using a GUID Partition Table (GPT) is recommended.

Once the memory stick is ready, you can do any of the following:
- Option A: Manually copy all files from the ISO to the formatted memory stick.
- Option B: Write the image to the memory stick with ddrescue, Passmark imageUSB, or similar.
- Option C: Use a bootable USB creation tool and select the ISO, or image as the source file, and the memory stick as the destination.

> ℹ Extended instructions [here](BOOTABLEUSB.md).

## Updating the BootROM

1. Remove the internal storage drive.
2. If you have a portable device, plug in the power adapter.
3. Insert your USB stick, then power on the device whilst holding `Option ⌥`.
4. Load into MacBRTool from the boot menu and let 'startup.nsh' run.
5. Type 'updatebr.nsh', then press return, the BootROM will then be updated (if necessary).
6. Type `exit` to leave the shell, or power down the device to complete the process.

**`startup.nsh` did not run:**\
In this case, you must manually find the USB filesystem. With the internal storage drive present, the filesystem is generally found at `fs7:`, in the shell type `fs7:`, then press return. With the internal storage drive removed, the filesystem is generally found at `fs0:`, in the shell type `fs0:`, then press return. A directory file list can be viewed by typing `ls`, then pressing return.

Once you find the filesystem with 'startup.nsh', you can then run the file.

## Compatibility

#### iMac

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

#### MacBook

```
MacBook6,1   Mac-F22CBAC8
MacBook7,1   Mac-F22CB9C8
MacBook8,1   Mac-BE0E8AC46FE800CC
MacBook9,1   Mac-9AE82516C7C6B903
MacBook10,1  Mac-EE2EBD4B90B839A8
```

#### MacBook Air

```
MacBookAir3,1   Mac-942452F5819B1C1B
MacBookAir4,1   Mac-742912EFDBEE19B3
MacBookAir5,1   Mac-2E6FAB96566FE58C
MacBookAir6,1   Mac-7DF21CB3ED6977E5
MacBookAir7,1   Mac-937CB26E2E02BB01
```

#### MacBook Pro

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

## Disclaimers

I'm not responsible if you do something wrong, if you're here I expect you to know what you're doing. Where I do my utmost to verify all information to my best ability, I'm not responsible for any mistakes my end either.

## Acknowledgements

> 🖼 Project icon by [Xcoder](https://macosicons.com/#/u/Xcoder) on macOSicons.

## Donate

<a href="https://www.buymeacoffee.com/Muerto"><img width="160" src="https://uc80e5ba3058c2d15b2a77972a8b.previews.dropboxusercontent.com/p/thumb/AB18JbfsN4REmFgvOrzwO3ooBl2K1VkxckN-h1H0qKcNhQDfIIROLC57mhfRHlNPZXBDEK7S3gHEnx6Uc35udaYsS-Mx66J6llYd_lSwfaIAntk3eynVXJNhd5nRHFDI1ncBuDVpVbrtKeQZlP2WPhejwCDH99YAFH8xcPef9q2d37EBjVV9-cK4cGUd7KmXCfa81wP6tXXV8r7-f_5L1c6tgs9HxLgqaDlAPXG8BcM9B6NRFdxlOsLGvYh9ESFE7fMb7dTrOu7PgsBsVrrIfTOxL8akUj2QiSGMJiZNXJrYrsW7mjKu_qQ-7Z-mhlZ2ZtY-FApmMFhfQrWj17D7hiXCemMdb_SaZCbaHBucMaJZ5Y1OPY3a6XlAxUCNJXSrFoI/p.png" alt="Buy Me A Coffee Logo" vspace="5" hspace="5"></a><a href="https://www.paypal.com/donate/?hosted_button_id=Z88F3UEZB47SQ"><img width="160" src="https://www.paypalobjects.com/webstatic/mktg/Logo/pp-logo-200px.png" alt="PayPal Logo" vspace="5" hspace="5"></a>

---