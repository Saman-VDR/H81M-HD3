H81M-HD3
========

DSDT and SSDT patches for Gigabyte's H81M-HD3 (rev. 1.0)

Used firmware version is F6 because F7 has write-protected nvram.

You can get a copy from https://www.gigabyte.com/Motherboard/GA-H81M-HD3-rev-10#support-dl-bios

But these patches should work for other Gigabyte 8 series boards, too.


Use [uefiTableExtract.pl](https://github.com/Saman-VDR/uefiTableExtract) to generate proper DSDT.dsl and SSDT*.dsl files.

In MaciASL open Preferences/Sources and add

    Name: H81M-HD3
    URL:  https://raw.githubusercontent.com/Saman-VDR/H81M-HD3/master

Apply patches and save to DSDT.aml


Open Dsdt2Bios and drag AmiBoardInfo.bin and DSDT.aml to the window.

A new AmiBoardInfo.bin (with your patched DSDT.aml inside) will created at the desktop.

Open your bios file in UEFITool and search for TEXT AmiBoardInfo
Replace body with AmiBoardInfo.bin 

![alt tag](https://cloud.githubusercontent.com/assets/3736530/11601050/eb48de5e-9ad0-11e5-9718-d4a353aff792.png)


To update your SSDT-SaSsdt.aml, search for GUID AAA99A23-13B6-4C31-BB8B-299E8EC04FA4

Replace body of raw section 0 with SSDT-SaSsdt.aml


To update your SSDT-CpuPm.aml, search for GUID 299141BB-211A-48A5-92C0-6F9A0A3A006E

Replace body of raw section 0 with SSDT-CpuPm.aml


##### Other useful tools:
* Dsdt2Bios
* MaciASL - https://github.com/acidanthera/MaciASL/releases
* UEFITool - https://github.com/LongSoft/UEFITool/releases
* UEFIExtract - https://github.com/LongSoft/UEFITool/releases

