## Que 5: What is UEFI? Difference between UEFI and BIOS?

> UEFI stands for Unified Extensible Firmware Interface. It does the same job as a BIOS, but with one basic difference: it stores all data about initialization and startup in an .efi file, instead of storing it on the firmware.
> This .efi file is stored on a special partition called EFI System Partition (ESP) on the hard disk. This ESP partition also contains the bootloader.

Benefits of UEFI over BIOS
1. UEFI supports drive sizes upto `9ZB`, whereas BIOS only supports `2.2TB`
2. UEFI provides faster boot time whereas BIOS is slow because it can't initiallize multiple hardware devices at once.
3. UEFI provide GUI as it runs on 32bit or 64bit mode whereas BIOS runs in 16bit and only allow keyboard for navigation
4. UEFI offers security like "Secure Boot", which prevents the computer from booting from unauthorized/unsigned applications. 
