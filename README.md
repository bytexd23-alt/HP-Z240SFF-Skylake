**HP-Z240SFF-Skylake Hackintosh**
-
Do not just copy this EFI and expect it to work.

Setup
-
To run Big Sur please put XCHI-Unsupported.kext

Create USB Installer
-
**Windows**
- https://dortania.github.io/OpenCore-Install-Guide/installer-guide/winblows-install.html, Follow this guide to add macOS to the USB.
- Copy the EFI
- You will need to generate a MacPro17,1 SMBIOS using GenSMBIOS.

**MacOS**
- https://dortania.github.io/OpenCore-Install-Guide/installer-guide/mac-install.html#setting-up-the-installer, Follow this guide to add macOS to the USB.
- Mount the EFI Partition.
- Copy the EFI files from the release file into your EFI partition.
- You will need to generate a MacPro17,1 SMBIOS using GenSMBIOS.

Before Booting
-
**Edit Bios**
- Note: Most of these options may not be present in your firmware, we recommend matching up as closely as possible but don't be too concerned if many of these options are not available in your BIOS

**Disable**

    Fast Boot
    Secure Boot
    Serial/COM Port
    Parallel Port
    VT-d (can be enabled if you set DisableIoMapper to YES)
    CSM
    Intel SGX
    Intel Platform Trust

**Enable**

    VT-x
    DVMT Pre-Allocated(iGPU Memory): 64MB
    SATA Mode: AHCI
Now you're ready to rock!

Post Install
-
https://dortania.github.io/OpenCore-Post-Install/ - Steps are outlined in this guide.
Mount your drives EFI partition and copy the contents of your USB installer's EFI partition to your drives EFI Partition.
Convert fron the debug version of opencore to the release version, cleanup logging etc. Follow This Guide.
Follow any other steps you would like to complete your hackintosh.

Audio
-
I have now managed to get Audio fully working with VoodooHDA.

My System
-
- Intel Xeon (Skylake)
- Intel P530 iGPU
- 8GB RAM

Important
-
- Connecting to a USB 3.0 port you will get the error 'Still waiting for root device'
