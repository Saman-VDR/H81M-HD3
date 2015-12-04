H81M-HD3
========

DSDT and SSDT patches for Gigabyte's H81M-HD3.

These patches should work for other 8 series boards, too.


Use [uefiTableExtract.pl](https://github.com/Saman-VDR/uefiTableExtract) to generate proper DSDT.dsl and SSDT*.dsl files.

In MaciASL open Preferences/Sources and add

    Name: H81M-HD3
    URL:  https://raw.githubusercontent.com/Saman-VDR/H81M-HD3/master

Apply patches and save to DSDT.aml


Open Dsdt2Bios and drag AmiBoardInfo.bin and DSDT.aml to the window.

A new AmiBoardInfo.bin (with your patched DSDT.aml inside) will created at the desktop.

Open your bios file in UEFITool and replace AmiBoardInfo.bin 

![alt tag](https://cloud.githubusercontent.com/assets/3736530/11601050/eb48de5e-9ad0-11e5-9718-d4a353aff792.png)


##### Other useful tools:
* Dsdt2Bios
* MaciASL - https://bitbucket.org/RehabMan/os-x-maciasl-patchmatic/downloads
* UEFITool - https://github.com/LongSoft/UEFITool/releases
* UEFIExtract - https://github.com/LongSoft/UEFITool/releases

