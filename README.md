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

Open your bios in UEFITool and replace AmiBoardInfo.bin 


##### Other useful tools:
* Dsdt2Bios
* MaciASL
* UEFITool
* UEFIExtract

