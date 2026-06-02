

~ 

❯ lsblk -o NAME,SIZE,FSTYPE,MOUNTPOINT,MODEL

NAME           SIZE FSTYPE   MOUNTPOINT                           MODEL

loop0           74M squashfs /snap/core22/2411                    

loop1         66.8M squashfs /snap/core24/1643                    

loop2            4K squashfs /snap/bare/5                         

loop3         91.7M squashfs /snap/gtk-common-themes/1535         

loop4        606.1M squashfs /snap/gnome-46-2404/153              

loop5         47.9M squashfs /snap/cups/1206                      

loop6       1009.1M squashfs /snap/onlyoffice-desktopeditors/1220 

loop7          395M squashfs /snap/mesa-2404/1165                 

loop8         49.3M squashfs /snap/snapd/26865                    

sda           29.7G                                               SD/MMC/MS PRO

└─sda1        29.7G vfat     /run/media/zek/SECFI-ZEK             

sdb          115.3G                                               DataTraveler 3.0

nvme0n1      953.9G                                               PC SN530 NVMe WDC 1024GB

├─nvme0n1p1    976M vfat     /boot/efi                            

├─nvme0n1p2  937.2G ext4     /                                    

└─nvme0n1p3   15.7G swap     [SWAP]                               



~ 

❯ sudo fdisk -l

[sudo] password for zek: 

Disk /dev/nvme0n1: 953.87 GiB, 1024209543168 bytes, 2000409264 sectors

Disk model: PC SN530 NVMe WDC 1024GB                

Units: sectors of 1 * 512 = 512 bytes

Sector size (logical/physical): 512 bytes / 512 bytes

I/O size (minimum/optimal): 512 bytes / 512 bytes

Disklabel type: gpt

Disk identifier: B86FF98E-BC95-44AB-9A99-6AD99D7DF7AD



Device              Start        End    Sectors   Size Type

/dev/nvme0n1p1       2048    2000895    1998848   976M EFI System

/dev/nvme0n1p2    2000896 1967382527 1965381632 937.2G Linux filesystem

/dev/nvme0n1p3 1967382528 2000408575   33026048  15.7G Linux swap





Disk /dev/loop0: 73.98 MiB, 77574144 bytes, 151512 sectors

Units: sectors of 1 * 512 = 512 bytes

Sector size (logical/physical): 512 bytes / 512 bytes

I/O size (minimum/optimal): 512 bytes / 512 bytes





Disk /dev/loop1: 66.8 MiB, 70049792 bytes, 136816 sectors

Units: sectors of 1 * 512 = 512 bytes

Sector size (logical/physical): 512 bytes / 512 bytes

I/O size (minimum/optimal): 512 bytes / 512 bytes





Disk /dev/loop2: 4 KiB, 4096 bytes, 8 sectors

Units: sectors of 1 * 512 = 512 bytes

Sector size (logical/physical): 512 bytes / 512 bytes

I/O size (minimum/optimal): 512 bytes / 512 bytes





Disk /dev/loop3: 91.69 MiB, 96141312 bytes, 187776 sectors

Units: sectors of 1 * 512 = 512 bytes

Sector size (logical/physical): 512 bytes / 512 bytes

I/O size (minimum/optimal): 512 bytes / 512 bytes





Disk /dev/loop4: 606.08 MiB, 635518976 bytes, 1241248 sectors

Units: sectors of 1 * 512 = 512 bytes

Sector size (logical/physical): 512 bytes / 512 bytes

I/O size (minimum/optimal): 512 bytes / 512 bytes





Disk /dev/loop5: 47.9 MiB, 50229248 bytes, 98104 sectors

Units: sectors of 1 * 512 = 512 bytes

Sector size (logical/physical): 512 bytes / 512 bytes

I/O size (minimum/optimal): 512 bytes / 512 bytes





Disk /dev/loop6: 1009.14 MiB, 1058164736 bytes, 2066728 sectors

Units: sectors of 1 * 512 = 512 bytes

Sector size (logical/physical): 512 bytes / 512 bytes

I/O size (minimum/optimal): 512 bytes / 512 bytes





Disk /dev/loop7: 394.98 MiB, 414167040 bytes, 808920 sectors

Units: sectors of 1 * 512 = 512 bytes

Sector size (logical/physical): 512 bytes / 512 bytes

I/O size (minimum/optimal): 512 bytes / 512 bytes





Disk /dev/loop8: 49.26 MiB, 51654656 bytes, 100888 sectors

Units: sectors of 1 * 512 = 512 bytes

Sector size (logical/physical): 512 bytes / 512 bytes

I/O size (minimum/optimal): 512 bytes / 512 bytes





Disk /dev/sda: 29.71 GiB, 31902400512 bytes, 62309376 sectors

Disk model: SD/MMC/MS PRO   

Units: sectors of 1 * 512 = 512 bytes

Sector size (logical/physical): 512 bytes / 512 bytes

I/O size (minimum/optimal): 512 bytes / 512 bytes

Disklabel type: dos

Disk identifier: 0x00000000



Device     Boot Start      End  Sectors  Size Id Type

/dev/sda1          63 62309375 62309313 29.7G  c W95 FAT32 (LBA)





Disk /dev/sdb: 115.29 GiB, 123790786560 bytes, 241778880 sectors

Disk model: DataTraveler 3.0

Units: sectors of 1 * 512 = 512 bytes

Sector size (logical/physical): 512 bytes / 512 bytes

I/O size (minimum/optimal): 512 bytes / 512 bytes

Disklabel type: dos

Disk identifier: 0x29657f3c



~ 

❯ lsusb

Bus 001 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub

Bus 002 Device 001: ID 1d6b:0003 Linux Foundation 3.0 root hub

Bus 003 Device 001: ID 1d6b:0002 Linux Foundation 2.0 root hub

Bus 003 Device 003: ID 27c6:639c Shenzhen Goodix Technology Co.,Ltd. Goodix USB2.0 MISC

Bus 003 Device 004: ID 0c45:6a10 Microdia Integrated_Webcam_HD

Bus 003 Device 005: ID 8087:0026 Intel Corp. AX201 Bluetooth

Bus 003 Device 006: ID 0bda:0177 Realtek Semiconductor Corp. USB2.0-CRW

Bus 004 Device 001: ID 1d6b:0003 Linux Foundation 3.0 root hub

Bus 004 Device 006: ID 0951:1666 Kingston Technology DataTraveler 100 G3/G4/SE9 G2/50 Kyson



~ 

❯ sudo dmesg -w

[    0.000000] Linux version 6.18.12+kali-amd64 (devel@kali.org) (x86_64-linux-gnu-gcc-15 (Debian 15.2.0-13) 15.2.0, GNU ld (GNU Binutils for Debian) 2.46) #1 SMP PREEMPT_DYNAMIC Kali 6.18.12-1kali1 (2026-02-25)

[    0.000000] Command line: BOOT_IMAGE=/boot/vmlinuz-6.18.12+kali-amd64 root=UUID=6640197b-a4e2-4071-9bb1-47aaf3d802ab ro quiet mitigations=off splash

[    0.000000] x86/split lock detection: #AC: crashing the kernel on kernel split_locks and warning on user-space split_locks

[    0.000000] BIOS-provided physical RAM map:

[    0.000000] BIOS-e820: [mem 0x0000000000000000-0x000000000009efff] usable

[    0.000000] BIOS-e820: [mem 0x000000000009f000-0x00000000000fffff] reserved

[    0.000000] BIOS-e820: [mem 0x0000000000100000-0x0000000060728fff] usable

[    0.000000] BIOS-e820: [mem 0x0000000060729000-0x0000000064510fff] reserved

[    0.000000] BIOS-e820: [mem 0x0000000064511000-0x0000000064d71fff] ACPI NVS

[    0.000000] BIOS-e820: [mem 0x0000000064d72000-0x0000000064ffefff] ACPI data

[    0.000000] BIOS-e820: [mem 0x0000000064fff000-0x0000000064ffffff] usable

[    0.000000] BIOS-e820: [mem 0x0000000065000000-0x0000000068ffffff] reserved

[    0.000000] BIOS-e820: [mem 0x0000000069400000-0x00000000695fffff] reserved

[    0.000000] BIOS-e820: [mem 0x0000000069e00000-0x00000000707fffff] reserved

[    0.000000] BIOS-e820: [mem 0x00000000c0000000-0x00000000cfffffff] reserved

[    0.000000] BIOS-e820: [mem 0x00000000fed20000-0x00000000fed7ffff] reserved

[    0.000000] BIOS-e820: [mem 0x00000000ff000000-0x00000000ffffffff] reserved

[    0.000000] BIOS-e820: [mem 0x0000000100000000-0x000000048f7fffff] usable

[    0.000000] NX (Execute Disable) protection: active

[    0.000000] APIC: Static calls initialized

[    0.000000] efi: EFI v2.7 by Dell

[    0.000000] efi: ACPI=0x64ffe000 ACPI 2.0=0x64ffe014 SMBIOS=0x60e74000 TPMFinalLog=0x64ce8000 ESRT=0x60d30c18 MEMATTR=0x5bd6c298 INITRD=0x5bd69098 RNG=0x64f6b018 TPMEventLog=0x64f5f018 

[    0.000000] random: crng init done

[    0.000000] efi: Remove mem99: MMIO range=[0xc0000000-0xcfffffff] (256MB) from e820 map

[    0.000000] e820: remove [mem 0xc0000000-0xcfffffff] reserved

[    0.000000] efi: Remove mem101: MMIO range=[0xff000000-0xffffffff] (16MB) from e820 map

[    0.000000] e820: remove [mem 0xff000000-0xffffffff] reserved

[    0.000000] secureboot: Secure boot disabled

[    0.000000] SMBIOS 3.2 present.

[    0.000000] DMI: Dell Inc. Inspiron 15 5510/076F7Y, BIOS 2.33.1 04/30/2025

[    0.000000] DMI: Memory slots populated: 2/2

[    0.000000] tsc: Detected 2900.000 MHz processor

[    0.000000] tsc: Detected 2918.400 MHz TSC

[    0.000008] e820: update [mem 0x00000000-0x00000fff] usable ==> reserved

[    0.000011] e820: remove [mem 0x000a0000-0x000fffff] usable

[    0.000017] last_pfn = 0x48f800 max_arch_pfn = 0x400000000

[    0.000021] MTRR map: 5 entries (3 fixed + 2 variable; max 23), built from 10 variable MTRRs

[    0.000023] x86/PAT: Configuration [0-7]: WB  WC  UC- UC  WB  WP  UC- WT  

[    0.000489] last_pfn = 0x65000 max_arch_pfn = 0x400000000

[    0.010721] esrt: Reserving ESRT space from 0x0000000060d30c18 to 0x0000000060d30ca0.

[    0.010733] Using GB pages for direct mapping

[    0.011019] RAMDISK: [mem 0x4a50d000-0x56f40fff]

[    0.011368] ACPI: Early table checksum verification disabled

[    0.011371] ACPI: RSDP 0x0000000064FFE014 000024 (v02 DELL  )

[    0.011375] ACPI: XSDT 0x0000000064F72188 000114 (v01 DELL   Dell Inc 00000002      01000013)

[    0.011381] ACPI: FACP 0x0000000064FF2000 000114 (v06 DELL   Dell Inc 00000002      01000013)

[    0.011385] ACPI: DSDT 0x0000000064F90000 05F62B (v02 DELL   Dell Inc 00000002      01000013)

[    0.011388] ACPI: FACS 0x0000000064D1B000 000040

[    0.011391] ACPI: SSDT 0x0000000064FFA000 0024D0 (v02 CpuRef CpuSsdt  00003000 INTL 20191018)

[    0.011394] ACPI: SSDT 0x0000000064FF3000 006F39 (v02 DptfTb DptfTabl 00001000 INTL 20191018)

[    0.011396] ACPI: HPET 0x0000000064FF1000 000038 (v01 DELL   Dell Inc 00000002      01000013)

[    0.011399] ACPI: APIC 0x0000000064FF0000 00012C (v04 DELL   Dell Inc 00000002      01000013)

[    0.011402] ACPI: SSDT 0x0000000064F8F000 000A65 (v02 DELL   DellRtd3 00001000 INTL 20191018)

[    0.011404] ACPI: NHLT 0x0000000064F8D000 001B54 (v00 DELL   Dell Inc 00000002      01000013)

[    0.011407] ACPI: SSDT 0x0000000064F8C000 00007B (v02 SaSsdt SaSsdt   00003000 INTL 20191018)

[    0.011409] ACPI: SSDT 0x0000000064F8A000 0012D2 (v02 INTEL  IgfxSsdt 00003000 INTL 20191018)

[    0.011412] ACPI: SSDT 0x0000000064F7E000 00B392 (v02 INTEL  TcssSsdt 00001000 INTL 20191018)

[    0.011415] ACPI: SSDT 0x0000000064F7D000 000D58 (v02 DELL   UsbCTabl 00001000 INTL 20191018)

[    0.011417] ACPI: LPIT 0x0000000064F7C000 0000CC (v01 DELL   Dell Inc 00000002      01000013)

[    0.011424] ACPI: WSMT 0x0000000064F7B000 000028 (v01 DELL   Dell Inc 00000002      01000013)

[    0.011428] ACPI: SSDT 0x0000000064F7A000 000B75 (v02 DELL   PtidDevc 00001000 INTL 20191018)

[    0.011431] ACPI: SSDT 0x0000000064F79000 00012A (v02 DELL   TbtTypeC 00000000 INTL 20191018)

[    0.011433] ACPI: DBGP 0x0000000064F78000 000034 (v01 DELL   Dell Inc 00000002      01000013)

[    0.011436] ACPI: DBG2 0x0000000064F77000 000054 (v00 DELL   Dell Inc 00000002      01000013)

[    0.011438] ACPI: BOOT 0x0000000064F76000 000028 (v01 DELL   CBX3     00000002      01000013)

[    0.011441] ACPI: SSDT 0x0000000064F75000 00060E (v02 DELL   Tpm2Tabl 00001000 INTL 20191018)

[    0.011443] ACPI: TPM2 0x0000000064F74000 00004C (v04 DELL   Dell Inc 00000002      01000013)

[    0.011446] ACPI: MSDM 0x0000000064F73000 000055 (v03 DELL   CBX3     06222004 AMI  00010013)

[    0.011449] ACPI: DMAR 0x0000000064FFD000 0000A0 (v02 INTEL  Dell Inc 00000002      01000013)

[    0.011451] ACPI: SSDT 0x0000000064F71000 000EC7 (v02 DELL   xh_Dell_ 00000000 INTL 20191018)

[    0.011454] ACPI: MCFG 0x0000000064F70000 00003C (v01                 00000001      00000000)

[    0.011456] ACPI: SSDT 0x0000000064F6F000 000144 (v02 Intel  ADebTabl 00001000 INTL 20191018)

[    0.011459] ACPI: UEFI 0x0000000064CE3000 00063A (v01 INTEL  RstVmdE  00000000 ??   00000000)

[    0.011462] ACPI: UEFI 0x0000000064CE2000 00005C (v01 INTEL  RstVmdV  00000000 ??   00000000)

[    0.011464] ACPI: PTDT 0x0000000064F6E000 000D44 (v00 DELL   Dell Inc 00000005 MSFT 0100000D)

[    0.011467] ACPI: BGRT 0x0000000064F6D000 000038 (v01 DELL   Dell Inc 00000002      01000013)

[    0.011469] ACPI: FPDT 0x0000000064F6C000 000034 (v01 DELL   Dell Inc 00000002      01000013)

[    0.011471] ACPI: Reserving FACP table memory at [mem 0x64ff2000-0x64ff2113]

[    0.011472] ACPI: Reserving DSDT table memory at [mem 0x64f90000-0x64fef62a]

[    0.011473] ACPI: Reserving FACS table memory at [mem 0x64d1b000-0x64d1b03f]

[    0.011474] ACPI: Reserving SSDT table memory at [mem 0x64ffa000-0x64ffc4cf]

[    0.011474] ACPI: Reserving SSDT table memory at [mem 0x64ff3000-0x64ff9f38]

[    0.011475] ACPI: Reserving HPET table memory at [mem 0x64ff1000-0x64ff1037]

[    0.011476] ACPI: Reserving APIC table memory at [mem 0x64ff0000-0x64ff012b]

[    0.011476] ACPI: Reserving SSDT table memory at [mem 0x64f8f000-0x64f8fa64]

[    0.011477] ACPI: Reserving NHLT table memory at [mem 0x64f8d000-0x64f8eb53]

[    0.011477] ACPI: Reserving SSDT table memory at [mem 0x64f8c000-0x64f8c07a]

[    0.011478] ACPI: Reserving SSDT table memory at [mem 0x64f8a000-0x64f8b2d1]

[    0.011479] ACPI: Reserving SSDT table memory at [mem 0x64f7e000-0x64f89391]

[    0.011479] ACPI: Reserving SSDT table memory at [mem 0x64f7d000-0x64f7dd57]

[    0.011480] ACPI: Reserving LPIT table memory at [mem 0x64f7c000-0x64f7c0cb]

[    0.011481] ACPI: Reserving WSMT table memory at [mem 0x64f7b000-0x64f7b027]

[    0.011481] ACPI: Reserving SSDT table memory at [mem 0x64f7a000-0x64f7ab74]

[    0.011482] ACPI: Reserving SSDT table memory at [mem 0x64f79000-0x64f79129]

[    0.011482] ACPI: Reserving DBGP table memory at [mem 0x64f78000-0x64f78033]

[    0.011483] ACPI: Reserving DBG2 table memory at [mem 0x64f77000-0x64f77053]

[    0.011484] ACPI: Reserving BOOT table memory at [mem 0x64f76000-0x64f76027]

[    0.011484] ACPI: Reserving SSDT table memory at [mem 0x64f75000-0x64f7560d]

[    0.011485] ACPI: Reserving TPM2 table memory at [mem 0x64f74000-0x64f7404b]

[    0.011485] ACPI: Reserving MSDM table memory at [mem 0x64f73000-0x64f73054]

[    0.011486] ACPI: Reserving DMAR table memory at [mem 0x64ffd000-0x64ffd09f]

[    0.011487] ACPI: Reserving SSDT table memory at [mem 0x64f71000-0x64f71ec6]

[    0.011487] ACPI: Reserving MCFG table memory at [mem 0x64f70000-0x64f7003b]

[    0.011488] ACPI: Reserving SSDT table memory at [mem 0x64f6f000-0x64f6f143]

[    0.011488] ACPI: Reserving UEFI table memory at [mem 0x64ce3000-0x64ce3639]

[    0.011489] ACPI: Reserving UEFI table memory at [mem 0x64ce2000-0x64ce205b]

[    0.011490] ACPI: Reserving PTDT table memory at [mem 0x64f6e000-0x64f6ed43]

[    0.011490] ACPI: Reserving BGRT table memory at [mem 0x64f6d000-0x64f6d037]

[    0.011491] ACPI: Reserving FPDT table memory at [mem 0x64f6c000-0x64f6c033]

[    0.011722] No NUMA configuration found

[    0.011723] Faking a node at [mem 0x0000000000000000-0x000000048f7fffff]

[    0.011732] NODE_DATA(0) allocated [mem 0x48f7d3500-0x48f7fdfff]

[    0.011924] Zone ranges:

[    0.011924]   DMA      [mem 0x0000000000001000-0x0000000000ffffff]

[    0.011926]   DMA32    [mem 0x0000000001000000-0x00000000ffffffff]

[    0.011927]   Normal   [mem 0x0000000100000000-0x000000048f7fffff]

[    0.011929]   Device   empty

[    0.011929] Movable zone start for each node

[    0.011931] Early memory node ranges

[    0.011931]   node   0: [mem 0x0000000000001000-0x000000000009efff]

[    0.011932]   node   0: [mem 0x0000000000100000-0x0000000060728fff]

[    0.011933]   node   0: [mem 0x0000000064fff000-0x0000000064ffffff]

[    0.011934]   node   0: [mem 0x0000000100000000-0x000000048f7fffff]

[    0.011937] Initmem setup node 0 [mem 0x0000000000001000-0x000000048f7fffff]

[    0.011942] On node 0, zone DMA: 1 pages in unavailable ranges

[    0.011975] On node 0, zone DMA: 97 pages in unavailable ranges

[    0.014194] On node 0, zone DMA32: 18646 pages in unavailable ranges

[    0.014443] On node 0, zone Normal: 12288 pages in unavailable ranges

[    0.014455] On node 0, zone Normal: 2048 pages in unavailable ranges

[    0.014477] Reserving Intel graphics memory at [mem 0x6c800000-0x707fffff]

[    0.014765] ACPI: PM-Timer IO Port: 0x1808

[    0.014773] ACPI: LAPIC_NMI (acpi_id[0x01] high edge lint[0x1])

[    0.014774] ACPI: LAPIC_NMI (acpi_id[0x02] high edge lint[0x1])

[    0.014775] ACPI: LAPIC_NMI (acpi_id[0x03] high edge lint[0x1])

[    0.014775] ACPI: LAPIC_NMI (acpi_id[0x04] high edge lint[0x1])

[    0.014776] ACPI: LAPIC_NMI (acpi_id[0x05] high edge lint[0x1])

[    0.014776] ACPI: LAPIC_NMI (acpi_id[0x06] high edge lint[0x1])

[    0.014777] ACPI: LAPIC_NMI (acpi_id[0x07] high edge lint[0x1])

[    0.014777] ACPI: LAPIC_NMI (acpi_id[0x08] high edge lint[0x1])

[    0.014778] ACPI: LAPIC_NMI (acpi_id[0x09] high edge lint[0x1])

[    0.014778] ACPI: LAPIC_NMI (acpi_id[0x0a] high edge lint[0x1])

[    0.014779] ACPI: LAPIC_NMI (acpi_id[0x0b] high edge lint[0x1])

[    0.014779] ACPI: LAPIC_NMI (acpi_id[0x0c] high edge lint[0x1])

[    0.014780] ACPI: LAPIC_NMI (acpi_id[0x0d] high edge lint[0x1])

[    0.014780] ACPI: LAPIC_NMI (acpi_id[0x0e] high edge lint[0x1])

[    0.014781] ACPI: LAPIC_NMI (acpi_id[0x0f] high edge lint[0x1])

[    0.014781] ACPI: LAPIC_NMI (acpi_id[0x10] high edge lint[0x1])

[    0.014818] IOAPIC[0]: apic_id 2, version 32, address 0xfec00000, GSI 0-119

[    0.014821] ACPI: INT_SRC_OVR (bus 0 bus_irq 0 global_irq 2 dfl dfl)

[    0.014823] ACPI: INT_SRC_OVR (bus 0 bus_irq 9 global_irq 9 high level)

[    0.014826] ACPI: Using ACPI (MADT) for SMP configuration information

[    0.014827] ACPI: HPET id: 0x8086a201 base: 0xfed00000

[    0.014836] e820: update [mem 0x5bace000-0x5bb56fff] usable ==> reserved

[    0.014843] TSC deadline timer available

[    0.014847] CPU topo: Max. logical packages:   1

[    0.014847] CPU topo: Max. logical dies:       1

[    0.014848] CPU topo: Max. dies per package:   1

[    0.014852] CPU topo: Max. threads per core:   2

[    0.014852] CPU topo: Num. cores per package:     4

[    0.014853] CPU topo: Num. threads per package:   8

[    0.014853] CPU topo: Allowing 8 present CPUs plus 0 hotplug CPUs

[    0.014866] PM: hibernation: Registered nosave memory: [mem 0x00000000-0x00000fff]

[    0.014867] PM: hibernation: Registered nosave memory: [mem 0x0009f000-0x000fffff]

[    0.014869] PM: hibernation: Registered nosave memory: [mem 0x5bace000-0x5bb56fff]

[    0.014870] PM: hibernation: Registered nosave memory: [mem 0x60729000-0x64ffefff]

[    0.014871] PM: hibernation: Registered nosave memory: [mem 0x65000000-0xffffffff]

[    0.014873] [mem 0x70800000-0xfed1ffff] available for PCI devices

[    0.014874] Booting paravirtualized kernel on bare hardware

[    0.014876] clocksource: refined-jiffies: mask: 0xffffffff max_cycles: 0xffffffff, max_idle_ns: 7645519600211568 ns

[    0.020248] setup_percpu: NR_CPUS:8192 nr_cpumask_bits:8 nr_cpu_ids:8 nr_node_ids:1

[    0.020539] percpu: Embedded 62 pages/cpu s217088 r8192 d28672 u262144

[    0.020545] pcpu-alloc: s217088 r8192 d28672 u262144 alloc=1*2097152

[    0.020547] pcpu-alloc: [0] 0 1 2 3 4 5 6 7 

[    0.020562] Kernel command line: BOOT_IMAGE=/boot/vmlinuz-6.18.12+kali-amd64 root=UUID=6640197b-a4e2-4071-9bb1-47aaf3d802ab ro quiet mitigations=off splash

[    0.020622] Unknown kernel command line parameters "splash", will be passed to user space.

[    0.020634] printk: log buffer data + meta data: 131072 + 458752 = 589824 bytes

[    0.022176] Dentry cache hash table entries: 2097152 (order: 12, 16777216 bytes, linear)

[    0.022904] Inode-cache hash table entries: 1048576 (order: 11, 8388608 bytes, linear)

[    0.023035] software IO TLB: area num 8.

[    0.034475] Fallback order for Node 0: 0 

[    0.034480] Built 1 zonelists, mobility grouping on.  Total pages: 4128456

[    0.034481] Policy zone: Normal

[    0.034489] mem auto-init: stack:all(zero), heap alloc:on, heap free:off

[    0.039220] SLUB: HWalign=64, Order=0-3, MinObjects=0, CPUs=8, Nodes=1

[    0.047100] ftrace: allocating 48103 entries in 188 pages

[    0.047103] ftrace: allocated 188 pages with 5 groups

[    0.047629] Dynamic Preempt: lazy

[    0.047679] rcu: Preemptible hierarchical RCU implementation.

[    0.047680] rcu:     RCU restricting CPUs from NR_CPUS=8192 to nr_cpu_ids=8.

[    0.047681]  Trampoline variant of Tasks RCU enabled.

[    0.047682]  Rude variant of Tasks RCU enabled.

[    0.047682]  Tracing variant of Tasks RCU enabled.

[    0.047683] rcu: RCU calculated value of scheduler-enlistment delay is 25 jiffies.

[    0.047683] rcu: Adjusting geometry for rcu_fanout_leaf=16, nr_cpu_ids=8

[    0.047692] RCU Tasks: Setting shift to 3 and lim to 1 rcu_task_cb_adjust=1 rcu_task_cpu_ids=8.

[    0.047694] RCU Tasks Rude: Setting shift to 3 and lim to 1 rcu_task_cb_adjust=1 rcu_task_cpu_ids=8.

[    0.047695] RCU Tasks Trace: Setting shift to 3 and lim to 1 rcu_task_cb_adjust=1 rcu_task_cpu_ids=8.

[    0.052097] NR_IRQS: 524544, nr_irqs: 2048, preallocated irqs: 16

[    0.052404] rcu: srcu_init: Setting srcu_struct sizes based on contention.

[    0.052651] Console: colour dummy device 80x25

[    0.052654] printk: legacy console [tty0] enabled

[    0.052689] ACPI: Core revision 20250807

[    0.053023] hpet: HPET dysfunctional in PC10. Force disabled.

[    0.053101] APIC: Switch to symmetric I/O mode setup

[    0.053104] DMAR: Host address width 39

[    0.053105] DMAR: DRHD base: 0x000000fed90000 flags: 0x0

[    0.053111] DMAR: dmar0: reg_base_addr fed90000 ver 4:0 cap 1c0000c40660462 ecap 29a00f0505e

[    0.053113] DMAR: DRHD base: 0x000000fed84000 flags: 0x0

[    0.053117] DMAR: dmar1: reg_base_addr fed84000 ver 1:0 cap d2008c40660462 ecap f050da

[    0.053119] DMAR: DRHD base: 0x000000fed91000 flags: 0x1

[    0.053124] DMAR: dmar2: reg_base_addr fed91000 ver 1:0 cap d2008c40660462 ecap f050da

[    0.053126] DMAR: RMRR base: 0x0000006c000000 end: 0x000000707fffff

[    0.053128] DMAR-IR: IOAPIC id 2 under DRHD base  0xfed91000 IOMMU 2

[    0.053129] DMAR-IR: HPET id 0 under DRHD base 0xfed91000

[    0.053130] DMAR-IR: Queued invalidation will be enabled to support x2apic and Intr-remapping.

[    0.055367] DMAR-IR: Enabled IRQ remapping in x2apic mode

[    0.055370] x2apic enabled

[    0.055459] APIC: Switched APIC routing to: cluster x2apic

[    0.060509] clocksource: tsc-early: mask: 0xffffffffffffffff max_cycles: 0x2a11290c0c8, max_idle_ns: 440795344938 ns

[    0.060516] Calibrating delay loop (skipped), value calculated using timer frequency.. 5836.80 BogoMIPS (lpj=11673600)

[    0.060550] CPU0: Thermal monitoring enabled (TM1)

[    0.060552] x86/cpu: User Mode Instruction Prevention (UMIP) activated

[    0.060666] CET detected: Indirect Branch Tracking enabled

[    0.060667] Last level iTLB entries: 4KB 0, 2MB 0, 4MB 0

[    0.060668] Last level dTLB entries: 4KB 0, 2MB 0, 4MB 0, 1GB 0

[    0.060671] process: using mwait in idle threads

[    0.060673] mitigations: Enabled attack vectors: SMT mitigations: off

[    0.060675] Speculative Store Bypass: Vulnerable

[    0.060677] Spectre V2 : Vulnerable

[    0.060677] ITS: Vulnerable

[    0.060678] Spectre V2 : User space: Vulnerable

[    0.060679] Spectre V1 : Vulnerable: __user pointer sanitization and usercopy barriers only; no swapgs barriers

[    0.060681] GDS: Vulnerable

[    0.060690] x86/fpu: Supporting XSAVE feature 0x001: 'x87 floating point registers'

[    0.060691] x86/fpu: Supporting XSAVE feature 0x002: 'SSE registers'

[    0.060692] x86/fpu: Supporting XSAVE feature 0x004: 'AVX registers'

[    0.060693] x86/fpu: Supporting XSAVE feature 0x020: 'AVX-512 opmask'

[    0.060694] x86/fpu: Supporting XSAVE feature 0x040: 'AVX-512 Hi256'

[    0.060695] x86/fpu: Supporting XSAVE feature 0x080: 'AVX-512 ZMM_Hi256'

[    0.060695] x86/fpu: Supporting XSAVE feature 0x200: 'Protection Keys User registers'

[    0.060696] x86/fpu: Supporting XSAVE feature 0x800: 'Control-flow User registers'

[    0.060697] x86/fpu: Supporting XSAVE feature 0x1000: 'Control-flow Kernel registers (KVM only)'

[    0.060698] x86/fpu: xstate_offset[2]:  576, xstate_sizes[2]:  256

[    0.060699] x86/fpu: xstate_offset[5]:  832, xstate_sizes[5]:   64

[    0.060700] x86/fpu: xstate_offset[6]:  896, xstate_sizes[6]:  512

[    0.060701] x86/fpu: xstate_offset[7]: 1408, xstate_sizes[7]: 1024

[    0.060702] x86/fpu: xstate_offset[9]: 2432, xstate_sizes[9]:    8

[    0.060703] x86/fpu: xstate_offset[11]: 2440, xstate_sizes[11]:   16

[    0.060704] x86/fpu: xstate_offset[12]: 2456, xstate_sizes[12]:   24

[    0.060705] x86/fpu: Enabled xstate features 0x1ae7, context size is 2480 bytes, using 'compacted' format.

[    0.064513] Freeing SMP alternatives memory: 44K

[    0.064513] pid_max: default: 32768 minimum: 301

[    0.064513] LSM: initializing lsm=lockdown,capability,landlock,yama,apparmor,tomoyo,bpf,ipe,ima,evm

[    0.064513] landlock: Up and running.

[    0.064513] Yama: disabled by default; enable with sysctl kernel.yama.*

[    0.064513] AppArmor: AppArmor initialized

[    0.064513] TOMOYO Linux initialized

[    0.064513] LSM support for eBPF active

[    0.064513] Mount-cache hash table entries: 32768 (order: 6, 262144 bytes, linear)

[    0.064513] Mountpoint-cache hash table entries: 32768 (order: 6, 262144 bytes, linear)

[    0.064513] smpboot: CPU0: 11th Gen Intel(R) Core(TM) i7-11390H @ 3.40GHz (family: 0x6, model: 0x8c, stepping: 0x2)

[    0.064513] Performance Events: PEBS fmt4+-baseline,  AnyThread deprecated, Icelake events, 32-deep LBR, full-width counters, Intel PMU driver.

[    0.064513] ... version:                   5

[    0.064513] ... bit width:                 48

[    0.064513] ... generic counters:          8

[    0.064513] ... generic bitmap:            00000000000000ff

[    0.064513] ... fixed-purpose counters:    4

[    0.064513] ... fixed-purpose bitmap:      000000000000000f

[    0.064513] ... value mask:                0000ffffffffffff

[    0.064513] ... max period:                00007fffffffffff

[    0.064513] ... global_ctrl mask:          0001000f000000ff

[    0.064513] signal: max sigframe size: 3632

[    0.064513] Estimated ratio of average max frequency by base frequency (times 1024): 1694

[    0.064513] rcu: Hierarchical SRCU implementation.

[    0.064513] rcu:     Max phase no-delay instances is 1000.

[    0.064513] Timer migration: 1 hierarchy levels; 8 children per group; 1 crossnode level

[    0.064513] NMI watchdog: Enabled. Permanently consumes one hw-PMU counter.

[    0.064513] smp: Bringing up secondary CPUs ...

[    0.064513] smpboot: x86: Booting SMP configuration:

[    0.064513] .... node  #0, CPUs:      #1 #2 #3 #4 #5 #6 #7

[    0.069922] smp: Brought up 1 node, 8 CPUs

[    0.069922] smpboot: Total of 8 processors activated (46694.40 BogoMIPS)

[    0.090255] node 0 deferred pages initialised in 16ms

[    0.090258] Memory: 15887288K/16513824K available (17655K kernel code, 3334K rwdata, 12852K rodata, 4448K init, 3624K bss, 610716K reserved, 0K cma-reserved)

[    0.090258] devtmpfs: initialized

[    0.090258] x86/mm: Memory block size: 128MB

[    0.090258] ACPI: PM: Registering ACPI NVS region [mem 0x64511000-0x64d71fff] (8785920 bytes)

[    0.090258] clocksource: jiffies: mask: 0xffffffff max_cycles: 0xffffffff, max_idle_ns: 7645041785100000 ns

[    0.090258] posixtimers hash table entries: 4096 (order: 4, 65536 bytes, linear)

[    0.090258] futex hash table entries: 2048 (131072 bytes on 1 NUMA nodes, total 128 KiB, linear).

[    0.090258] pinctrl core: initialized pinctrl subsystem

[    0.092707] NET: Registered PF_NETLINK/PF_ROUTE protocol family

[    0.092942] DMA: preallocated 2048 KiB GFP_KERNEL pool for atomic allocations

[    0.093060] DMA: preallocated 2048 KiB GFP_KERNEL|GFP_DMA pool for atomic allocations

[    0.093185] DMA: preallocated 2048 KiB GFP_KERNEL|GFP_DMA32 pool for atomic allocations

[    0.093198] audit: initializing netlink subsys (disabled)

[    0.093210] audit: type=2000 audit(1780405985.032:1): state=initialized audit_enabled=0 res=1

[    0.093210] thermal_sys: Registered thermal governor 'fair_share'

[    0.093210] thermal_sys: Registered thermal governor 'bang_bang'

[    0.093210] thermal_sys: Registered thermal governor 'step_wise'

[    0.093210] thermal_sys: Registered thermal governor 'user_space'

[    0.093210] thermal_sys: Registered thermal governor 'power_allocator'

[    0.093210] cpuidle: using governor ladder

[    0.093210] cpuidle: using governor menu

[    0.093210] Simple Boot Flag at 0x47 set to 0x80

[    0.093210] acpiphp: ACPI Hot Plug PCI Controller Driver version: 0.5

[    0.093210] PCI: ECAM [mem 0xc0000000-0xc38fffff] (base 0xc0000000) for domain 0000 [bus 00-38]

[    0.093210] PCI: Using configuration type 1 for base access

[    0.093210] kprobes: kprobe jump-optimization is enabled. All kprobes are optimized if possible.

[    0.093210] HugeTLB: registered 1.00 GiB page size, pre-allocated 0 pages

[    0.093210] HugeTLB: 16380 KiB vmemmap can be freed for a 1.00 GiB page

[    0.093210] HugeTLB: registered 2.00 MiB page size, pre-allocated 0 pages

[    0.093210] HugeTLB: 28 KiB vmemmap can be freed for a 2.00 MiB page

[    0.093210] ACPI: Added _OSI(Module Device)

[    0.093210] ACPI: Added _OSI(Processor Device)

[    0.093210] ACPI: Added _OSI(Processor Aggregator Device)

[    0.153471] ACPI: 13 ACPI AML tables successfully acquired and loaded

[    0.165597] ACPI: Dynamic OEM Table Load:

[    0.165597] ACPI: SSDT 0xFFFF8E07C2551000 000496 (v02 PmRef  Cpu0Cst  00003001 INTL 20191018)

[    0.165795] ACPI: Dynamic OEM Table Load:

[    0.165801] ACPI: SSDT 0xFFFF8E07C2557800 000668 (v02 PmRef  Cpu0Ist  00003000 INTL 20191018)

[    0.166585] ACPI: Dynamic OEM Table Load:

[    0.166590] ACPI: SSDT 0xFFFF8E07C1A1B400 0001CB (v02 PmRef  Cpu0Psd  00003000 INTL 20191018)

[    0.167300] ACPI: Dynamic OEM Table Load:

[    0.167305] ACPI: SSDT 0xFFFF8E07C1A7CC00 00028B (v02 PmRef  Cpu0Hwp  00003000 INTL 20191018)

[    0.169407] ACPI: Dynamic OEM Table Load:

[    0.169413] ACPI: SSDT 0xFFFF8E07C254F000 0008E7 (v02 PmRef  ApIst    00003000 INTL 20191018)

[    0.170253] ACPI: Dynamic OEM Table Load:

[    0.170258] ACPI: SSDT 0xFFFF8E07C2552800 00048A (v02 PmRef  ApHwp    00003000 INTL 20191018)

[    0.171049] ACPI: Dynamic OEM Table Load:

[    0.171054] ACPI: SSDT 0xFFFF8E07C2554800 0004D4 (v02 PmRef  ApPsd    00003000 INTL 20191018)

[    0.171836] ACPI: Dynamic OEM Table Load:

[    0.171841] ACPI: SSDT 0xFFFF8E07C2556800 00048A (v02 PmRef  ApCst    00003000 INTL 20191018)

[    0.172515] ACPI: EC: EC started

[    0.172515] ACPI: EC: interrupt blocked

[    0.173836] ACPI: EC: EC_CMD/EC_SC=0x934, EC_DATA=0x930

[    0.173838] ACPI: \_SB_.PC00.LPCB.ECDV: Boot DSDT EC used to handle transactions

[    0.173839] ACPI: Interpreter enabled

[    0.173895] ACPI: PM: (supports S0 S4 S5)

[    0.173896] ACPI: Using IOAPIC for interrupt routing

[    0.173946] PCI: Using host bridge windows from ACPI; if necessary, use "pci=nocrs" and report a bug

[    0.173948] PCI: Ignoring E820 reservations for host bridge windows

[    0.174843] ACPI: Enabled 8 GPEs in block 00 to 7F

[    0.178416] ACPI: \_SB_.PC00.XHCI.RHUB.HS10.BTRT: New power resource

[    0.186482] ACPI: \_SB_.PC00.SAT0.VOL0.V0PR: New power resource

[    0.186568] ACPI: \_SB_.PC00.SAT0.VOL1.V1PR: New power resource

[    0.186643] ACPI: \_SB_.PC00.SAT0.VOL2.V2PR: New power resource

[    0.191557] ACPI: \_SB_.PC00.CNVW.WRST: New power resource

[    0.198721] ACPI: \_SB_.PC00.TBT0: New power resource

[    0.198751] ACPI: \_SB_.PC00.TBT1: New power resource

[    0.198779] ACPI: \_SB_.PC00.D3C_: New power resource

[    0.313931] ACPI: \PIN_: New power resource

[    0.314414] ACPI: PCI Root Bridge [PC00] (domain 0000 [bus 00-38])

[    0.314419] acpi PNP0A08:00: _OSC: OS supports [ExtendedConfig ASPM ClockPM Segments MSI HPX-Type3]

[    0.316007] acpi PNP0A08:00: _OSC: platform does not support [AER]

[    0.319238] acpi PNP0A08:00: _OSC: OS now controls [PCIeHotplug SHPCHotplug PME PCIeCapability LTR]

[    0.322286] PCI host bridge to bus 0000:00

[    0.322289] pci_bus 0000:00: root bus resource [io  0x0000-0x0cf7 window]

[    0.322291] pci_bus 0000:00: root bus resource [io  0x0d00-0xffff window]

[    0.322292] pci_bus 0000:00: root bus resource [mem 0x000a0000-0x000bffff window]

[    0.322293] pci_bus 0000:00: root bus resource [mem 0x70800000-0xbfffffff window]

[    0.322295] pci_bus 0000:00: root bus resource [mem 0x4000000000-0x7fffffffff window]

[    0.322296] pci_bus 0000:00: root bus resource [bus 00-38]

[    0.322396] pci 0000:00:00.0: [8086:9a14] type 00 class 0x060000 conventional PCI endpoint

[    0.322525] pci 0000:00:02.0: [8086:9a49] type 00 class 0x030000 PCIe Root Complex Integrated Endpoint

[    0.322542] pci 0000:00:02.0: BAR 0 [mem 0x6024000000-0x6024ffffff 64bit]

[    0.322545] pci 0000:00:02.0: BAR 2 [mem 0x4000000000-0x400fffffff 64bit pref]

[    0.322546] pci 0000:00:02.0: BAR 4 [io  0x3000-0x303f]

[    0.322558] pci 0000:00:02.0: DMAR: Skip IOMMU disabling for graphics

[    0.322560] pci 0000:00:02.0: Video device with shadowed ROM at [mem 0x000c0000-0x000dffff]

[    0.322592] pci 0000:00:02.0: VF BAR 0 [mem 0x00000000-0x00ffffff 64bit]

[    0.322593] pci 0000:00:02.0: VF BAR 0 [mem 0x00000000-0x06ffffff 64bit]: contains BAR 0 for 7 VFs

[    0.322595] pci 0000:00:02.0: VF BAR 2 [mem 0x00000000-0x1fffffff 64bit pref]

[    0.322596] pci 0000:00:02.0: VF BAR 2 [mem 0x00000000-0xdfffffff 64bit pref]: contains BAR 2 for 7 VFs

[    0.322714] pci 0000:00:04.0: [8086:9a03] type 00 class 0x118000 conventional PCI endpoint

[    0.322752] pci 0000:00:04.0: BAR 0 [mem 0x6025240000-0x602525ffff 64bit]

[    0.322974] pci 0000:00:07.0: [8086:9a23] type 01 class 0x060400 PCIe Root Port

[    0.322994] pci 0000:00:07.0: PCI bridge to [bus 01-38]

[    0.322999] pci 0000:00:07.0:   bridge window [mem 0x74000000-0x8a0fffff]

[    0.323007] pci 0000:00:07.0:   bridge window [mem 0x6000000000-0x6021ffffff 64bit pref]

[    0.323031] pci 0000:00:07.0: Overriding RP PIO Log Size to 4

[    0.323090] pci 0000:00:07.0: PME# supported from D0 D3hot D3cold

[    0.323578] pci 0000:00:08.0: [8086:9a11] type 00 class 0x088000 conventional PCI endpoint

[    0.323597] pci 0000:00:08.0: BAR 0 [mem 0x60252aa000-0x60252aafff 64bit]

[    0.323678] pci 0000:00:0a.0: [8086:9a0d] type 00 class 0x118000 PCIe Root Complex Integrated Endpoint

[    0.323696] pci 0000:00:0a.0: BAR 0 [mem 0x6025290000-0x6025297fff 64bit]

[    0.323702] pci 0000:00:0a.0: enabling Extended Tags

[    0.323792] pci 0000:00:0d.0: [8086:9a13] type 00 class 0x0c0330 conventional PCI endpoint

[    0.323822] pci 0000:00:0d.0: BAR 0 [mem 0x6025280000-0x602528ffff 64bit]

[    0.323856] pci 0000:00:0d.0: PME# supported from D3hot D3cold

[    0.324068] pci 0000:00:0d.2: [8086:9a1b] type 00 class 0x0c0340 conventional PCI endpoint

[    0.324093] pci 0000:00:0d.2: BAR 0 [mem 0x6025200000-0x602523ffff 64bit]

[    0.324095] pci 0000:00:0d.2: BAR 2 [mem 0x60252a9000-0x60252a9fff 64bit]

[    0.324122] pci 0000:00:0d.2: supports D1 D2

[    0.324124] pci 0000:00:0d.2: PME# supported from D0 D1 D2 D3hot D3cold

[    0.324246] pci 0000:00:0e.0: [8086:9a0b] type 00 class 0x010400 PCIe Root Complex Integrated Endpoint

[    0.324274] pci 0000:00:0e.0: BAR 0 [mem 0x6022000000-0x6023ffffff 64bit]

[    0.324275] pci 0000:00:0e.0: BAR 2 [mem 0x8c000000-0x8dffffff]

[    0.324279] pci 0000:00:0e.0: BAR 4 [mem 0x6025100000-0x60251fffff 64bit]

[    0.324470] pci 0000:00:12.0: [8086:a0fc] type 00 class 0x070000 conventional PCI endpoint

[    0.324523] pci 0000:00:12.0: BAR 0 [mem 0x6025270000-0x602527ffff 64bit]

[    0.324569] pci 0000:00:12.0: PME# supported from D0 D3hot

[    0.324890] pci 0000:00:14.0: [8086:a0ed] type 00 class 0x0c0330 conventional PCI endpoint

[    0.324938] pci 0000:00:14.0: BAR 0 [mem 0x6025260000-0x602526ffff 64bit]

[    0.324996] pci 0000:00:14.0: PME# supported from D3hot D3cold

[    0.325229] pci 0000:00:14.2: [8086:a0ef] type 00 class 0x050000 conventional PCI endpoint

[    0.325280] pci 0000:00:14.2: BAR 0 [mem 0x60252a0000-0x60252a3fff 64bit]

[    0.325284] pci 0000:00:14.2: BAR 2 [mem 0x60252a8000-0x60252a8fff 64bit]

[    0.325414] pci 0000:00:14.3: [8086:a0f0] type 00 class 0x028000 PCIe Root Complex Integrated Endpoint

[    0.325483] pci 0000:00:14.3: BAR 0 [mem 0x602529c000-0x602529ffff 64bit]

[    0.325581] pci 0000:00:14.3: PME# supported from D0 D3hot D3cold

[    0.325833] pci 0000:00:15.0: [8086:a0e8] type 00 class 0x0c8000 conventional PCI endpoint

[    0.325896] pci 0000:00:15.0: BAR 0 [mem 0x00000000-0x00000fff 64bit]

[    0.336688] pci 0000:00:15.1: [8086:a0e9] type 00 class 0x0c8000 conventional PCI endpoint

[    0.336766] pci 0000:00:15.1: BAR 0 [mem 0x00000000-0x00000fff 64bit]

[    0.348706] pci 0000:00:16.0: [8086:a0e0] type 00 class 0x078000 conventional PCI endpoint

[    0.348762] pci 0000:00:16.0: BAR 0 [mem 0x60252a5000-0x60252a5fff 64bit]

[    0.348822] pci 0000:00:16.0: PME# supported from D3hot

[    0.349141] pci 0000:00:1f.0: [8086:a082] type 00 class 0x060100 conventional PCI endpoint

[    0.349400] pci 0000:00:1f.3: [8086:a0c8] type 00 class 0x040100 conventional PCI endpoint

[    0.349501] pci 0000:00:1f.3: BAR 0 [mem 0x6025298000-0x602529bfff 64bit]

[    0.349514] pci 0000:00:1f.3: BAR 4 [mem 0x6025000000-0x60250fffff 64bit]

[    0.349611] pci 0000:00:1f.3: PME# supported from D3hot D3cold

[    0.349926] pci 0000:00:1f.4: [8086:a0a3] type 00 class 0x0c0500 conventional PCI endpoint

[    0.349975] pci 0000:00:1f.4: BAR 0 [mem 0x60252a4000-0x60252a40ff 64bit]

[    0.349982] pci 0000:00:1f.4: BAR 4 [io  0xefa0-0xefbf]

[    0.350138] pci 0000:00:1f.5: [8086:a0a4] type 00 class 0x0c8000 conventional PCI endpoint

[    0.350193] pci 0000:00:1f.5: BAR 0 [mem 0xfe010000-0xfe010fff]

[    0.350280] pci 0000:00:07.0: PCI bridge to [bus 01-38]

[    0.360692] Low-power S0 idle used by default for system suspend

[    0.367439] ACPI: EC: interrupt unblocked

[    0.367440] ACPI: EC: event unblocked

[    0.367452] ACPI: EC: EC_CMD/EC_SC=0x934, EC_DATA=0x930

[    0.367453] ACPI: EC: GPE=0x6e

[    0.367454] ACPI: \_SB_.PC00.LPCB.ECDV: Boot DSDT EC initialization complete

[    0.367455] ACPI: \_SB_.PC00.LPCB.ECDV: EC: Used to handle transactions and events

[    0.367617] iommu: Default domain type: Translated

[    0.367617] iommu: DMA domain TLB invalidation policy: lazy mode

[    0.367617] pps_core: LinuxPPS API ver. 1 registered

[    0.367617] pps_core: Software ver. 5.3.6 - Copyright 2005-2007 Rodolfo Giometti <giometti@linux.it>

[    0.367617] PTP clock support registered

[    0.367617] EDAC MC: Ver: 3.0.0

[    0.367617] efivars: Registered efivars operations

[    0.368553] NetLabel: Initializing

[    0.368554] NetLabel:  domain hash size = 128

[    0.368555] NetLabel:  protocols = UNLABELED CIPSOv4 CALIPSO

[    0.368570] NetLabel:  unlabeled traffic allowed by default

[    0.368574] PCI: Using ACPI for IRQ routing

[    0.370521] PCI: pci_cache_line_size set to 64 bytes

[    0.370581] pci 0000:00:1f.5: BAR 0 [mem 0xfe010000-0xfe010fff]: can't claim; no compatible bridge window

[    0.370629] e820: reserve RAM buffer [mem 0x0009f000-0x0009ffff]

[    0.370631] e820: reserve RAM buffer [mem 0x5bace000-0x5bffffff]

[    0.370632] e820: reserve RAM buffer [mem 0x60729000-0x63ffffff]

[    0.370632] e820: reserve RAM buffer [mem 0x65000000-0x67ffffff]

[    0.370633] e820: reserve RAM buffer [mem 0x48f800000-0x48fffffff]

[    0.370655] pci 0000:00:02.0: vgaarb: setting as boot VGA device

[    0.370655] pci 0000:00:02.0: vgaarb: bridge control possible

[    0.370655] pci 0000:00:02.0: vgaarb: VGA device added: decodes=io+mem,owns=io+mem,locks=none

[    0.370655] vgaarb: loaded

[    0.370655] Monitor-Mwait will be used to enter C-1 state

[    0.370655] Monitor-Mwait will be used to enter C-2 state

[    0.370655] Monitor-Mwait will be used to enter C-3 state

[    0.370655] clocksource: Switched to clocksource tsc-early

[    0.370655] VFS: Disk quotas dquot_6.6.0

[    0.370655] VFS: Dquot-cache hash table entries: 512 (order 0, 4096 bytes)

[    0.370655] AppArmor: AppArmor Filesystem Enabled

[    0.370655] pnp: PnP ACPI init

[    0.370655] system 00:00: [io  0x0680-0x069f] has been reserved

[    0.370655] system 00:00: [io  0x164e-0x164f] has been reserved

[    0.370655] pnp 00:04: disabling [mem 0xc0000000-0xcfffffff] because it overlaps 0000:00:02.0 BAR 9 [mem 0x00000000-0xdfffffff 64bit pref]

[    0.370655] system 00:04: [mem 0xfedc0000-0xfedc7fff] has been reserved

[    0.370655] system 00:04: [mem 0xfeda0000-0xfeda0fff] has been reserved

[    0.370655] system 00:04: [mem 0xfeda1000-0xfeda1fff] has been reserved

[    0.370655] system 00:04: [mem 0xfed20000-0xfed7ffff] could not be reserved

[    0.370655] system 00:04: [mem 0xfed90000-0xfed93fff] could not be reserved

[    0.370655] system 00:04: [mem 0xfed45000-0xfed8ffff] could not be reserved

[    0.370655] system 00:04: [mem 0xfee00000-0xfeefffff] has been reserved

[    0.370674] system 00:05: [io  0x1800-0x18fe] could not be reserved

[    0.370675] system 00:05: [mem 0xfe000000-0xfe01ffff] has been reserved

[    0.370677] system 00:05: [mem 0xfe04c000-0xfe04ffff] has been reserved

[    0.370678] system 00:05: [mem 0xfe050000-0xfe0affff] has been reserved

[    0.370679] system 00:05: [mem 0xfe0d0000-0xfe0fffff] has been reserved

[    0.370680] system 00:05: [mem 0xfe200000-0xfe7fffff] has been reserved

[    0.370682] system 00:05: [mem 0xff000000-0xffffffff] has been reserved

[    0.370683] system 00:05: [mem 0xfd000000-0xfd68ffff] has been reserved

[    0.370684] system 00:05: [mem 0xfd6b0000-0xfd6cffff] has been reserved

[    0.370685] system 00:05: [mem 0xfd6f0000-0xfdffffff] has been reserved

[    0.370918] system 00:06: [io  0x2000-0x20fe] has been reserved

[    0.373497] pnp: PnP ACPI: found 8 devices

[    0.378814] clocksource: acpi_pm: mask: 0xffffff max_cycles: 0xffffff, max_idle_ns: 2085701024 ns

[    0.378857] NET: Registered PF_INET protocol family

[    0.378995] IP idents hash table entries: 262144 (order: 9, 2097152 bytes, linear)

[    0.389036] tcp_listen_portaddr_hash hash table entries: 8192 (order: 5, 131072 bytes, linear)

[    0.389059] Table-perturb hash table entries: 65536 (order: 6, 262144 bytes, linear)

[    0.389096] TCP established hash table entries: 131072 (order: 8, 1048576 bytes, linear)

[    0.389277] TCP bind hash table entries: 65536 (order: 9, 2097152 bytes, linear)

[    0.389404] TCP: Hash tables configured (established 131072 bind 65536)

[    0.389471] MPTCP token hash table entries: 16384 (order: 7, 393216 bytes, linear)

[    0.389524] UDP hash table entries: 8192 (order: 7, 524288 bytes, linear)

[    0.389603] UDP-Lite hash table entries: 8192 (order: 7, 524288 bytes, linear)

[    0.389666] NET: Registered PF_UNIX/PF_LOCAL protocol family

[    0.389672] NET: Registered PF_XDP protocol family

[    0.389678] pci_bus 0000:00: max bus depth: 1 pci_try_num: 2

[    0.389686] pci 0000:00:02.0: VF BAR 2 [mem 0x4020000000-0x40ffffffff 64bit pref]: assigned

[    0.389691] pci 0000:00:02.0: VF BAR 0 [mem 0x4010000000-0x4016ffffff 64bit]: assigned

[    0.389694] pci 0000:00:07.0: bridge window [io  0x4000-0x4fff]: assigned

[    0.389695] pci 0000:00:15.0: BAR 0 [mem 0x4017000000-0x4017000fff 64bit]: assigned

[    0.389716] pci 0000:00:15.1: BAR 0 [mem 0x4017001000-0x4017001fff 64bit]: assigned

[    0.389733] pci 0000:00:1f.5: BAR 0 [mem 0x70800000-0x70800fff]: assigned

[    0.389745] pci 0000:00:07.0: PCI bridge to [bus 01-38]

[    0.389747] pci 0000:00:07.0:   bridge window [io  0x4000-0x4fff]

[    0.389751] pci 0000:00:07.0:   bridge window [mem 0x74000000-0x8a0fffff]

[    0.389754] pci 0000:00:07.0:   bridge window [mem 0x6000000000-0x6021ffffff 64bit pref]

[    0.389759] pci_bus 0000:00: resource 4 [io  0x0000-0x0cf7 window]

[    0.389760] pci_bus 0000:00: resource 5 [io  0x0d00-0xffff window]

[    0.389761] pci_bus 0000:00: resource 6 [mem 0x000a0000-0x000bffff window]

[    0.389762] pci_bus 0000:00: resource 7 [mem 0x70800000-0xbfffffff window]

[    0.389763] pci_bus 0000:00: resource 8 [mem 0x4000000000-0x7fffffffff window]

[    0.389764] pci_bus 0000:01: resource 0 [io  0x4000-0x4fff]

[    0.389765] pci_bus 0000:01: resource 1 [mem 0x74000000-0x8a0fffff]

[    0.389766] pci_bus 0000:01: resource 2 [mem 0x6000000000-0x6021ffffff 64bit pref]

[    0.390193] PCI: CLS 0 bytes, default 64

[    0.390239] DMAR: No ATSR found

[    0.390240] DMAR: No SATC found

[    0.390241] DMAR: dmar1: Using Queued invalidation

[    0.390244] DMAR: dmar0: Using Queued invalidation

[    0.390246] DMAR: dmar2: Using Queued invalidation

[    0.390356] Trying to unpack rootfs image as initramfs...

[    0.390406] pci 0000:00:07.0: Adding to iommu group 0

[    0.390470] pci 0000:00:02.0: Adding to iommu group 1

[    0.390491] pci 0000:00:00.0: Adding to iommu group 2

[    0.390497] pci 0000:00:04.0: Adding to iommu group 3

[    0.390504] pci 0000:00:08.0: Adding to iommu group 4

[    0.390511] pci 0000:00:0a.0: Adding to iommu group 5

[    0.390522] pci 0000:00:0d.0: Adding to iommu group 6

[    0.390528] pci 0000:00:0d.2: Adding to iommu group 6

[    0.390536] pci 0000:00:0e.0: Adding to iommu group 7

[    0.390544] pci 0000:00:12.0: Adding to iommu group 8

[    0.390554] pci 0000:00:14.0: Adding to iommu group 9

[    0.390560] pci 0000:00:14.2: Adding to iommu group 9

[    0.390566] pci 0000:00:14.3: Adding to iommu group 10

[    0.390576] pci 0000:00:15.0: Adding to iommu group 11

[    0.390582] pci 0000:00:15.1: Adding to iommu group 11

[    0.390591] pci 0000:00:16.0: Adding to iommu group 12

[    0.390605] pci 0000:00:1f.0: Adding to iommu group 13

[    0.390612] pci 0000:00:1f.3: Adding to iommu group 13

[    0.390618] pci 0000:00:1f.4: Adding to iommu group 13

[    0.390625] pci 0000:00:1f.5: Adding to iommu group 13

[    0.391114] DMAR: Intel(R) Virtualization Technology for Directed I/O

[    0.391115] PCI-DMA: Using software bounce buffering for IO (SWIOTLB)

[    0.391116] software IO TLB: mapped [mem 0x000000004650d000-0x000000004a50d000] (64MB)

[    0.391144] clocksource: tsc: mask: 0xffffffffffffffff max_cycles: 0x2a11290c0c8, max_idle_ns: 440795344938 ns

[    0.391288] clocksource: Switched to clocksource tsc

[    0.404089] Initialise system trusted keyrings

[    0.404098] Key type blacklist registered

[    0.404212] workingset: timestamp_bits=36 max_order=22 bucket_order=0

[    0.404423] fuse: init (API version 7.45)

[    0.404604] integrity: Platform Keyring initialized

[    0.404606] integrity: Machine keyring initialized

[    0.415145] Key type asymmetric registered

[    0.415148] Asymmetric key parser 'x509' registered

[    0.415429] Block layer SCSI generic (bsg) driver version 0.4 loaded (major 245)

[    0.415510] io scheduler mq-deadline registered

[    0.424224] ledtrig-cpu: registered to indicate activity on CPUs

[    0.424516] pcieport 0000:00:07.0: PME: Signaling with IRQ 123

[    0.424536] pcieport 0000:00:07.0: pciehp: Slot #0 AttnBtn- PwrCtrl- MRL- AttnInd- PwrInd- HotPlug+ Surprise+ Interlock- NoCompl+ IbPresDis- LLActRep+

[    0.429238] Serial: 8250/16550 driver, 4 ports, IRQ sharing enabled

[    0.429569] serial 0000:00:12.0: enabling device (0000 -> 0002)

[    0.429841] hpet_acpi_add: no address or irqs in _CRS

[    0.429876] Linux agpgart interface v0.103

[    0.436487] i8042: PNP: PS/2 Controller [PNP0303:PS2K,PNP0f13:PS2M] at 0x60,0x64 irq 1,12

[    0.436812] i8042: Warning: Keylock active

[    0.438600] serio: i8042 KBD port at 0x60,0x64 irq 1

[    0.438604] serio: i8042 AUX port at 0x60,0x64 irq 12

[    0.438736] mousedev: PS/2 mouse device common for all mice

[    0.438750] rtc_cmos 00:01: RTC can wake from S4

[    0.439649] rtc_cmos 00:01: registered as rtc0

[    0.439827] rtc_cmos 00:01: setting system clock to 2026-06-02T13:13:05 UTC (1780405985)

[    0.439855] rtc_cmos 00:01: alarms up to one month, y3k, 242 bytes nvram

[    0.440620] input: AT Translated Set 2 keyboard as /devices/platform/i8042/serio0/input/input0

[    0.448175] intel_pstate: Intel P-state driver initializing

[    0.448703] intel_pstate: HWP enabled

[    0.448918] efifb: probing for efifb

[    0.448926] efifb: framebuffer at 0x4000000000, using 8100k, total 8100k

[    0.448928] efifb: mode is 1920x1080x32, linelength=7680, pages=1

[    0.448929] efifb: scrolling: redraw

[    0.448929] efifb: Truecolor: size=8:8:8:8, shift=24:16:8:0

[    0.449006] Console: switching to colour frame buffer device 240x67

[    0.450197] fb0: EFI VGA frame buffer device

[    0.450323] NET: Registered PF_INET6 protocol family

[    0.455143] Segment Routing with IPv6

[    0.455144] RPL Segment Routing with IPv6

[    0.455150] In-situ OAM (IOAM) with IPv6

[    0.455164] mip6: Mobile IPv6

[    0.455167] NET: Registered PF_PACKET protocol family

[    0.455185] mpls_gso: MPLS GSO support

[    0.463918] ENERGY_PERF_BIAS: Set to 'normal', was 'performance'

[    0.464256] microcode: Current revision: 0x0000003e

[    0.464259] microcode: Updated early from: 0x0000003c

[    0.480192] resctrl: L2 allocation detected

[    0.480210] IPI shorthand broadcast: enabled

[    0.481463] sched_clock: Marking stable (472271250, 7911668)->(517047598, -36864680)

[    0.481719] registered taskstats version 1

[    0.481827] Loading compiled-in X.509 certificates

[    0.753004] Freeing initrd memory: 207056K

[    0.779547] Loaded X.509 cert 'Build time autogenerated kernel key: 82748024bf97d64d411057d887546d2616b0506b'

[    0.780979] Demotion targets for Node 0: null

[    0.781013] Key type .fscrypt registered

[    0.781014] Key type fscrypt-provisioning registered

[    0.789584] Key type encrypted registered

[    0.789586] AppArmor: AppArmor sha256 policy hashing enabled

[    0.789712] integrity: Loading X.509 certificate: UEFI:db

[    0.789730] integrity: Loaded X.509 cert 'Dell Inc.: Dell Bios DB Key: 637fa7a9f74471b406de0511557071fd41dd5487'

[    0.789731] integrity: Loading X.509 certificate: UEFI:db

[    0.789738] integrity: Loaded X.509 cert 'Dell Inc.: Dell Bios FW Aux Authority 2018: dd4df7c3f5ce7e5a77847915abc37b031f6b10bd'

[    0.789739] integrity: Loading X.509 certificate: UEFI:db

[    0.789748] integrity: Loaded X.509 cert 'Microsoft Windows Production PCA 2011: a92902398e16c49778cd90f99e4f9ae17c55af53'

[    0.789749] integrity: Loading X.509 certificate: UEFI:db

[    0.789757] integrity: Loaded X.509 cert 'Microsoft Corporation UEFI CA 2011: 13adbf4309bd82709c8cd54f316ed522988a1bd4'

[    0.789758] integrity: Loading X.509 certificate: UEFI:db

[    0.789765] integrity: Loaded X.509 cert 'Microsoft Corporation: Windows UEFI CA 2023: aefc5fbbbe055d8f8daa585473499417ab5a5272'

[    0.789766] integrity: Loading X.509 certificate: UEFI:db

[    0.789775] integrity: Loaded X.509 cert 'Microsoft Option ROM UEFI CA 2023: 514fbf937fa46fb57bf07af8bed84b3b864b1711'

[    0.789775] integrity: Loading X.509 certificate: UEFI:db

[    0.789782] integrity: Loaded X.509 cert 'Microsoft UEFI CA 2023: 81aa6b3244c935bce0d6628af39827421e32497d'

[    0.790732] ima: Allocated hash algorithm: sha256

[    0.823068] ima: No architecture policies found

[    0.823081] evm: Initialising EVM extended attributes:

[    0.823082] evm: security.selinux

[    0.823083] evm: security.SMACK64 (disabled)

[    0.823083] evm: security.SMACK64EXEC (disabled)

[    0.823084] evm: security.SMACK64TRANSMUTE (disabled)

[    0.823085] evm: security.SMACK64MMAP (disabled)

[    0.823085] evm: security.apparmor

[    0.823086] evm: security.ima

[    0.823087] evm: security.capability

[    0.823087] evm: HMAC attrs: 0x1

[    0.827011] RAS: Correctable Errors collector initialized.

[    0.831730] clk: Disabling unused clocks

[    0.831732] PM: genpd: Disabling unused power domains

[    0.839454] Freeing unused decrypted memory: 2028K

[    0.840027] Freeing unused kernel image (initmem) memory: 4448K

[    0.840048] Write protecting the kernel read-only data: 32768k

[    0.840439] Freeing unused kernel image (text/rodata gap) memory: 776K

[    0.840768] Freeing unused kernel image (rodata/data gap) memory: 1484K

[    0.848862] x86/mm: Checked W+X mappings: passed, no W+X pages found.

[    0.848867] Run /init as init process

[    0.848868]   with arguments:

[    0.848869]     /init

[    0.848870]     splash

[    0.848871]   with environment:

[    0.848871]     HOME=/

[    0.848872]     TERM=linux

[    1.040835] vmd 0000:00:0e.0: PCI host bridge to bus 10000:e0

[    1.040843] pci_bus 10000:e0: root bus resource [bus e0-ff]

[    1.040846] pci_bus 10000:e0: root bus resource [mem 0x8c000000-0x8dffffff]

[    1.040848] pci_bus 10000:e0: root bus resource [mem 0x6025102000-0x60251fffff 64bit]

[    1.040878] pci 10000:e0:1c.0: [8086:09ab] type 00 class 0x088000 conventional PCI endpoint

[    1.044706] pci 10000:e0:1c.0: Adding to iommu group 7

[    1.044764] pci 10000:e0:1c.4: [8086:a0bc] type 01 class 0x060400 PCIe Root Port

[    1.044794] pci 10000:e0:1c.4: PCI bridge to [bus e1]

[    1.044802] pci 10000:e0:1c.4:   bridge window [io  0x0000-0x0fff]

[    1.044806] pci 10000:e0:1c.4:   bridge window [mem 0x8c000000-0x8c0fffff]

[    1.044887] pci 10000:e0:1c.4: PME# supported from D0 D3hot D3cold

[    1.044934] pci 10000:e0:1c.4: PTM enabled (root), 4ns granularity

[    1.045054] i801_smbus 0000:00:1f.4: enabling device (0000 -> 0003)

[    1.045177] wmi_bus wmi_bus-PNP0C14:02: [Firmware Bug]: WQBC data block query control method not found

[    1.045222] pci 10000:e0:1c.4: Adding to iommu group 7

[    1.045234] pci 10000:e0:1c.4: Primary bus is hard wired to 0

[    1.045242] i801_smbus 0000:00:1f.4: SPD Write Disable is set

[    1.045251] i801_smbus 0000:00:1f.4: SMBus using PCI interrupt

[    1.045308] pci 10000:e1:00.0: [15b7:5007] type 00 class 0x010802 PCIe Endpoint

[    1.045376] pci 10000:e1:00.0: BAR 0 [mem 0x8c000000-0x8c003fff 64bit]

[    1.045383] pci 10000:e1:00.0: BAR 4 [mem 0x00000000-0x000000ff 64bit]

[    1.045799] pci 10000:e1:00.0: Adding to iommu group 7

[    1.045845] pci 10000:e0:1c.4: PCI bridge to [bus e1]

[    1.045857] pci 10000:e0:1c.4: Primary bus is hard wired to 0

[    1.052928] intel-lpss 0000:00:15.0: enabling device (0000 -> 0002)

[    1.052974] i2c i2c-0: Successfully instantiated SPD at 0x50

[    1.053535] idma64 idma64.0: Found Intel integrated DMA 64-bit

[    1.059854] ACPI: bus type thunderbolt registered

[    1.063634] ACPI: bus type USB registered

[    1.063683] usbcore: registered new interface driver usbfs

[    1.063696] usbcore: registered new interface driver hub

[    1.063712] usbcore: registered new device driver usb

[    1.068516] intel-lpss 0000:00:15.1: enabling device (0000 -> 0002)

[    1.080000] input: Lid Switch as /devices/LNXSYSTM:00/LNXSYBUS:00/PNP0C0D:00/input/input2

[    1.080093] ACPI: button: Lid Switch [LID0]

[    1.080129] input: Power Button as /devices/LNXSYSTM:00/LNXSYBUS:00/PNP0C0C:00/input/input3

[    1.082641] ACPI: button: Power Button [PBTN]

[    1.082935] idma64 idma64.1: Found Intel integrated DMA 64-bit

[    1.083281] input: Sleep Button as /devices/LNXSYSTM:00/LNXSYBUS:00/PNP0C0E:00/input/input4

[    1.083309] ACPI: button: Sleep Button [SBTN]

[    1.111921] ACPI: battery: Slot [BAT0] (battery present)

[    1.120862] ACPI: bus type drm_connector registered

[    1.126678] iTCO_vendor_support: vendor-support=0

[    1.127827] xhci_hcd 0000:00:0d.0: xHCI Host Controller

[    1.127840] xhci_hcd 0000:00:0d.0: new USB bus registered, assigned bus number 1

[    1.128980] xhci_hcd 0000:00:0d.0: hcc params 0x20007fc1 hci version 0x120 quirks 0x0000000200009810

[    1.129354] xhci_hcd 0000:00:0d.0: xHCI Host Controller

[    1.129360] xhci_hcd 0000:00:0d.0: new USB bus registered, assigned bus number 2

[    1.129364] xhci_hcd 0000:00:0d.0: Host supports USB 3.1 Enhanced SuperSpeed

[    1.129466] usb usb1: New USB device found, idVendor=1d6b, idProduct=0002, bcdDevice= 6.18

[    1.129471] usb usb1: New USB device strings: Mfr=3, Product=2, SerialNumber=1

[    1.129474] usb usb1: Product: xHCI Host Controller

[    1.129476] usb usb1: Manufacturer: Linux 6.18.12+kali-amd64 xhci-hcd

[    1.129479] usb usb1: SerialNumber: 0000:00:0d.0

[    1.129649] hub 1-0:1.0: USB hub found

[    1.129664] hub 1-0:1.0: 1 port detected

[    1.130044] usb usb2: New USB device found, idVendor=1d6b, idProduct=0003, bcdDevice= 6.18

[    1.130048] usb usb2: New USB device strings: Mfr=3, Product=2, SerialNumber=1

[    1.130050] usb usb2: Product: xHCI Host Controller

[    1.130053] usb usb2: Manufacturer: Linux 6.18.12+kali-amd64 xhci-hcd

[    1.130055] usb usb2: SerialNumber: 0000:00:0d.0

[    1.130177] hub 2-0:1.0: USB hub found

[    1.130192] hub 2-0:1.0: 4 ports detected

[    1.131447] xhci_hcd 0000:00:14.0: xHCI Host Controller

[    1.131454] xhci_hcd 0000:00:14.0: new USB bus registered, assigned bus number 3

[    1.132629] xhci_hcd 0000:00:14.0: hcc params 0x20007fc1 hci version 0x120 quirks 0x0000100200009810

[    1.133033] xhci_hcd 0000:00:14.0: xHCI Host Controller

[    1.133037] xhci_hcd 0000:00:14.0: new USB bus registered, assigned bus number 4

[    1.133040] xhci_hcd 0000:00:14.0: Host supports USB 3.1 Enhanced SuperSpeed

[    1.133122] usb usb3: New USB device found, idVendor=1d6b, idProduct=0002, bcdDevice= 6.18

[    1.133126] usb usb3: New USB device strings: Mfr=3, Product=2, SerialNumber=1

[    1.133129] usb usb3: Product: xHCI Host Controller

[    1.133131] usb usb3: Manufacturer: Linux 6.18.12+kali-amd64 xhci-hcd

[    1.133134] usb usb3: SerialNumber: 0000:00:14.0

[    1.133304] hub 3-0:1.0: USB hub found

[    1.133332] hub 3-0:1.0: 12 ports detected

[    1.134811] iTCO_wdt iTCO_wdt: Found a Intel PCH TCO device (Version=6, TCOBASE=0x0400)

[    1.134923] iTCO_wdt iTCO_wdt: initialized. heartbeat=30 sec (nowayout=0)

[    1.135003] usb usb4: New USB device found, idVendor=1d6b, idProduct=0003, bcdDevice= 6.18

[    1.135007] usb usb4: New USB device strings: Mfr=3, Product=2, SerialNumber=1

[    1.135009] usb usb4: Product: xHCI Host Controller

[    1.135011] usb usb4: Manufacturer: Linux 6.18.12+kali-amd64 xhci-hcd

[    1.135013] usb usb4: SerialNumber: 0000:00:14.0

[    1.135163] hub 4-0:1.0: USB hub found

[    1.135184] hub 4-0:1.0: 4 ports detected

[    1.135849] hid: raw HID events driver (C) Jiri Kosina

[    1.208213] pci 10000:e0:1c.4: disabling bridge window [mem size 0x00000000 64bit pref disabled] to [bus e1] (unused)

[    1.208233] pci 10000:e0:1c.4: bridge window [mem 0x8c000000-0x8c0fffff]: assigned

[    1.208237] pci 10000:e0:1c.4: bridge window [io  size 0x1000]: can't assign; no space

[    1.208241] pci 10000:e0:1c.4: bridge window [io  size 0x1000]: failed to assign

[    1.208245] pci 10000:e0:1c.4: bridge window [io  size 0x1000]: can't assign; no space

[    1.208248] pci 10000:e0:1c.4: bridge window [io  size 0x1000]: failed to assign

[    1.208253] pci 10000:e1:00.0: BAR 0 [mem 0x8c000000-0x8c003fff 64bit]: assigned

[    1.208273] pci 10000:e1:00.0: BAR 4 [mem 0x8c004000-0x8c0040ff 64bit]: assigned

[    1.208291] pci 10000:e0:1c.4: PCI bridge to [bus e1]

[    1.208300] pci 10000:e0:1c.4:   bridge window [mem 0x8c000000-0x8c0fffff]

[    1.208327] pci 10000:e1:00.0: VMD: Default LTR value set by driver

[    1.208497] pcieport 10000:e0:1c.4: can't derive routing for PCI INT A

[    1.208501] pcieport 10000:e0:1c.4: PCI INT A: no GSI

[    1.208667] pcieport 10000:e0:1c.4: PME: Signaling with IRQ 176

[    1.208919] vmd 0000:00:0e.0: Bound to PCI domain 10000

[    1.244802] input: DELL0B24:00 04F3:3147 Mouse as /devices/pci0000:00/0000:00:15.1/i2c_designware.1/i2c-2/i2c-DELL0B24:00/0018:04F3:3147.0001/input/input6

[    1.244871] input: DELL0B24:00 04F3:3147 Touchpad as /devices/pci0000:00/0000:00:15.1/i2c_designware.1/i2c-2/i2c-DELL0B24:00/0018:04F3:3147.0001/input/input7

[    1.245786] hid-generic 0018:04F3:3147.0001: input,hidraw0: I2C HID v1.00 Mouse [DELL0B24:00 04F3:3147] on i2c-DELL0B24:00

[    1.260341] SCSI subsystem initialized

[    1.284378] libata version 3.00 loaded.

[    1.299071] input: DELL0B24:00 04F3:3147 Mouse as /devices/pci0000:00/0000:00:15.1/i2c_designware.1/i2c-2/i2c-DELL0B24:00/0018:04F3:3147.0001/input/input9

[    1.299164] input: DELL0B24:00 04F3:3147 Touchpad as /devices/pci0000:00/0000:00:15.1/i2c_designware.1/i2c-2/i2c-DELL0B24:00/0018:04F3:3147.0001/input/input10

[    1.299247] hid-multitouch 0018:04F3:3147.0001: input,hidraw0: I2C HID v1.00 Mouse [DELL0B24:00 04F3:3147] on i2c-DELL0B24:00

[    1.313152] Key type psk registered

[    1.337678] nvme nvme0: pci function 10000:e1:00.0

[    1.337691] pcieport 10000:e0:1c.4: can't derive routing for PCI INT A

[    1.337693] nvme 10000:e1:00.0: PCI INT A: no GSI

[    1.353112] nvme nvme0: allocated 64 MiB host memory buffer (1 segment).

[    1.354132] nvme nvme0: 8/0/0 default/read/poll queues

[    1.357572]  nvme0n1: p1 p2 p3

[    1.379967] usb 3-1: new low-speed USB device number 2 using xhci_hcd

[    1.520827] usb 3-1: New USB device found, idVendor=30fa, idProduct=1701, bcdDevice= 1.00

[    1.520843] usb 3-1: New USB device strings: Mfr=2, Product=1, SerialNumber=0

[    1.520845] usb 3-1: Product: USB GAMING MOUSE 

[    1.520847] usb 3-1: Manufacturer: INSTANT

[    1.639966] usb 3-5: new full-speed USB device number 3 using xhci_hcd

[    1.675726] input: PS/2 Generic Mouse as /devices/platform/i8042/serio1/input/input5

[    1.782182] usb 3-5: New USB device found, idVendor=27c6, idProduct=639c, bcdDevice= 1.00

[    1.782185] usb 3-5: New USB device strings: Mfr=1, Product=2, SerialNumber=3

[    1.782186] usb 3-5: Product: Goodix USB2.0 MISC

[    1.782187] usb 3-5: Manufacturer: Goodix Technology Co., Ltd.

[    1.782188] usb 3-5: SerialNumber: UIDCF0C7C5A_XXXX_MOC_B0

[    1.849686] ish-hid {33AECD58-B679-4E54-9BD9-A04D34F0C226}: [hid-ish]: enum_devices_done OK, num_hid_devices=1

[    1.850310] i915 0000:00:02.0: [drm] Found tigerlake/uy (device ID 9a49) integrated display version 12.00 stepping D0

[    1.850547] input: INSTANT USB GAMING MOUSE  as /devices/pci0000:00/0000:00:14.0/usb3/3-1/3-1:1.0/0003:30FA:1701.0002/input/input12

[    1.850614] hid-generic 0003:30FA:1701.0002: input,hidraw1: USB HID v1.10 Mouse [INSTANT USB GAMING MOUSE ] on usb-0000:00:14.0-1/input0

[    1.850851] i915 0000:00:02.0: [drm] VT-d active for gfx access

[    1.850926] Console: switching to colour dummy device 80x25

[    1.850949] i915 0000:00:02.0: vgaarb: deactivate vga console

[    1.851013] i915 0000:00:02.0: [drm] Using Transparent Hugepages

[    1.851475] i915 0000:00:02.0: vgaarb: VGA decodes changed: olddecodes=io+mem,decodes=io+mem:owns=io+mem

[    1.852544] i915 0000:00:02.0: [drm] Finished loading DMC firmware i915/tgl_dmc_ver2_12.bin (v2.12)

[    1.853524] input: INSTANT USB GAMING MOUSE  Keyboard as /devices/pci0000:00/0000:00:14.0/usb3/3-1/3-1:1.1/0003:30FA:1701.0003/input/input13

[    1.853755] hid-generic 001F:8087:0AC2.0004: hidraw2: SENSOR HUB HID v2.00 Device [hid-ishtp 8087:0AC2] on 

[    1.859225] hid-sensor-hub 001F:8087:0AC2.0004: hidraw2: SENSOR HUB HID v2.00 Device [hid-ishtp 8087:0AC2] on 

[    1.864753] i915 0000:00:02.0: [drm] Protected Xe Path (PXP) protected content support initialized

[    1.882380] i915 0000:00:02.0: [drm] Registered 4 planes with drm panic

[    1.882383] [drm] Initialized i915 1.6.0 for 0000:00:02.0 on minor 0

[    1.887722] ACPI: video: Video Device [GFX0] (multi-head: yes  rom: no  post: no)

[    1.893931] input: Video Bus as /devices/LNXSYSTM:00/LNXSYBUS:00/PNP0A08:00/LNXVIDEO:00/input/input15

[    1.908059] usb 3-6: new high-speed USB device number 4 using xhci_hcd

[    1.912014] hid-generic 0003:30FA:1701.0003: input,hiddev0,hidraw3: USB HID v1.10 Keyboard [INSTANT USB GAMING MOUSE ] on usb-0000:00:14.0-1/input1

[    1.912038] usbcore: registered new interface driver usbhid

[    1.912039] usbhid: USB HID core driver

[    1.917469] fbcon: i915drmfb (fb0) is primary device

[    1.931621] Console: switching to colour frame buffer device 240x67

[    1.950156] i915 0000:00:02.0: [drm] fb0: i915drmfb frame buffer device

[    2.054213] usb 3-6: New USB device found, idVendor=0c45, idProduct=6a10, bcdDevice= 2.71

[    2.054216] usb 3-6: New USB device strings: Mfr=2, Product=1, SerialNumber=0

[    2.054218] usb 3-6: Product: Integrated_Webcam_HD

[    2.054219] usb 3-6: Manufacturer: C7FJH68R1754302C40B0

[    2.176086] usb 3-10: new full-speed USB device number 5 using xhci_hcd

[    2.315158] usb 3-10: New USB device found, idVendor=8087, idProduct=0026, bcdDevice= 0.02

[    2.315161] usb 3-10: New USB device strings: Mfr=0, Product=0, SerialNumber=0

[    2.512017] raid6: avx512x4 gen() 49936 MB/s

[    2.580052] raid6: avx512x2 gen() 54615 MB/s

[    2.647924] raid6: avx512x1 gen() 44259 MB/s

[    2.716007] raid6: avx2x4   gen() 37734 MB/s

[    2.784004] raid6: avx2x2   gen() 36658 MB/s

[    2.851989] raid6: avx2x1   gen() 28970 MB/s

[    2.851991] raid6: using algorithm avx512x2 gen() 54615 MB/s

[    2.919917] raid6: .... xor() 31300 MB/s, rmw enabled

[    2.919918] raid6: using avx512x2 recovery algorithm

[    2.923673] xor: automatically using best checksumming function   avx       

[    2.926870] async_tx: api initialized (async)

[    3.176099] Btrfs loaded, zoned=yes, fsverity=yes

[    3.207616] PM: Image not found (code -22)

[    3.313850] EXT4-fs (nvme0n1p2): orphan cleanup on readonly fs

[    3.314207] EXT4-fs (nvme0n1p2): mounted filesystem 6640197b-a4e2-4071-9bb1-47aaf3d802ab ro with ordered data mode. Quota mode: none.

[    3.404679] Not activating Mandatory Access Control as /sbin/tomoyo-init does not exist.

[    3.444952] systemd[1]: Inserted module 'autofs4'

[    4.143366] systemd[1]: systemd 260.1-1 running in system mode (+PAM +AUDIT +SELINUX +APPARMOR +IMA +IPE +SMACK +SECCOMP +GCRYPT -GNUTLS +OPENSSL +ACL +BLKID +CURL +ELFUTILS +FIDO2 +IDN2 +KMOD +LIBCRYPTSETUP +LIBCRYPTSETUP_PLUGINS +LIBFDISK +PCRE2 +PWQUALITY +P11KIT +QRENCODE +TPM2 +BZIP2 +LZ4 +XZ +ZLIB +ZSTD +BPF_FRAMEWORK +BTF -XKBCOMMON -UTMP +LIBARCHIVE)

[    4.143382] systemd[1]: Detected architecture x86-64.

[    4.158228] systemd[1]: Hostname set to <kali>.

[    4.301696] systemd[1]: bpf-restrict-fs: LSM BPF program attached

[    4.378860] systemd-sslh-generator: Configuration directory '/etc/sslh/' does not exist! No units generated.

[    4.388009] (generato[404]: '/usr/lib/systemd/system-generators/systemd-sslh-generator' terminated by signal ABRT.

[    4.401366] systemd[1]: /usr/lib/systemd/system/system-xfs_scrub.slice:15: Support for option CPUAccounting= has been removed and it is ignored

[    4.415684] systemd[1]: /usr/lib/systemd/system/xfs_scrub_all.service:26: Support for option CPUAccounting= has been removed and it is ignored

[    4.468094] systemd[1]: Queued start job for default target graphical.target.

[    4.495064] systemd[1]: Created slice system-getty.slice - Slice /system/getty.

[    4.495337] systemd[1]: Created slice system-modprobe.slice - Slice /system/modprobe.

[    4.495547] systemd[1]: Created slice system-systemd\x2dfsck.slice - Slice /system/systemd-fsck.

[    4.495808] systemd[1]: Created slice system-xfs_scrub.slice - xfs_scrub background service slice.

[    4.495952] systemd[1]: Created slice user.slice - User and Session Slice.

[    4.495981] systemd[1]: Started systemd-ask-password-wall.path - Forward Password Requests to Wall Directory Watch.

[    4.496192] systemd[1]: Set up automount proc-sys-fs-binfmt_misc.automount - Arbitrary Executable File Formats File System Automount Point.

[    4.496204] systemd[1]: Expecting device dev-disk-by\x2duuid-47c6f212\x2df902\x2d40f0\x2d8bfd\x2db698bf2724f9.device - /dev/disk/by-uuid/47c6f212-f902-40f0-8bfd-b698bf2724f9...

[    4.496209] systemd[1]: Expecting device dev-disk-by\x2duuid-EB15\x2dEA10.device - /dev/disk/by-uuid/EB15-EA10...

[    4.496220] systemd[1]: Reached target imports.target - Image Downloads.

[    4.496236] systemd[1]: Reached target nss-user-lookup.target - User and Group Name Lookups.

[    4.496247] systemd[1]: Reached target slices.target - Slice Units.

[    4.496257] systemd[1]: Reached target stunnel.target - TLS tunnels for network services - per-config-file target.

[    4.496303] systemd[1]: Listening on dm-event.socket - Device-mapper event daemon FIFOs.

[    4.496345] systemd[1]: Listening on lvm2-lvmpolld.socket - LVM2 poll daemon socket.

[    4.496932] systemd[1]: Listening on systemd-ask-password.socket - Query the User Interactively for a Password.

[    4.497345] systemd[1]: Listening on systemd-creds.socket - Credential Encryption/Decryption.

[    4.497886] systemd[1]: Listening on systemd-factory-reset.socket - Factory Reset Management.

[    4.497931] systemd[1]: Listening on systemd-journald-dev-log.socket - Journal Socket (/dev/log).

[    4.497966] systemd[1]: Listening on systemd-journald.socket - Journal Sockets.

[    4.498623] systemd[1]: Listening on systemd-mute-console.socket - Console Output Muting Service Socket.

[    4.498643] systemd[1]: systemd-pcrextend.socket - TPM PCR Measurements skipped, unmet condition check ConditionSecurity=measured-uki

[    4.498650] systemd[1]: systemd-pcrlock.socket - Make TPM PCR Policy skipped, unmet condition check ConditionSecurity=measured-uki

[    4.498684] systemd[1]: Listening on systemd-udevd-control.socket - udev Control Socket.

[    4.498712] systemd[1]: Listening on systemd-udevd-kernel.socket - udev Kernel Socket.

[    4.498741] systemd[1]: Listening on systemd-udevd-varlink.socket - udev Varlink Socket.

[    4.498769] systemd[1]: Listening on systemd-userdbd.socket - User Database Manager Socket.

[    4.499345] systemd[1]: Mounting dev-hugepages.mount - Huge Pages File System...

[    4.499772] systemd[1]: Mounting dev-mqueue.mount - POSIX Message Queue File System...

[    4.500064] systemd[1]: Mounting proc-sys-fs-binfmt_misc.mount - /proc/sys/fs/binfmt_misc...

[    4.500415] systemd[1]: Mounting sys-kernel-debug.mount - Kernel Debug File System...

[    4.500907] systemd[1]: Mounting sys-kernel-tracing.mount - Kernel Trace File System...

[    4.500961] systemd[1]: auth-rpcgss-module.service - Kernel Module supporting RPCSEC_GSS skipped, unmet condition check ConditionPathExists=/etc/krb5.keytab

[    4.502070] systemd[1]: Starting keyboard-setup.service - Set the console keyboard layout...

[    4.502685] systemd[1]: Starting kmod-static-nodes.service - Create List of Static Device Nodes...

[    4.502718] systemd[1]: modprobe@configfs.service - Load Kernel Module configfs skipped, unmet condition check ConditionKernelModuleLoaded=!configfs

[    4.503105] systemd[1]: Mounting sys-kernel-config.mount - Kernel Configuration File System...

[    4.503132] systemd[1]: modprobe@drm.service - Load Kernel Module drm skipped, unmet condition check ConditionKernelModuleLoaded=!drm

[    4.503658] systemd[1]: Starting modprobe@efi_pstore.service - Load Kernel Module efi_pstore...

[    4.503680] systemd[1]: modprobe@fuse.service - Load Kernel Module fuse skipped, unmet condition check ConditionKernelModuleLoaded=!fuse

[    4.504250] systemd[1]: Mounting sys-fs-fuse-connections.mount - FUSE Control File System...

[    4.504346] systemd[1]: systemd-fsck-root.service - File System Check on Root Device skipped, unmet condition check ConditionPathExists=!/run/initramfs/fsck-root

[    4.504377] systemd[1]: systemd-hibernate-clear.service - Clear Stale Hibernate Storage Info skipped, unmet condition check ConditionPathExists=/sys/firmware/efi/efivars/HibernateLocation-8cf2644b-4b0b-428f-9387-6d876050dc67

[    4.506363] systemd[1]: Starting systemd-journald.service - Journal Service...

[    4.507950] systemd[1]: Starting systemd-modules-load.service - Load Kernel Modules...

[    4.507976] systemd[1]: systemd-pcrmachine.service - TPM PCR Machine ID Measurement skipped, unmet condition check ConditionSecurity=measured-uki

[    4.508009] systemd[1]: systemd-pcrproduct.service - TPM NvPCR Product ID Measurement skipped, unmet condition check ConditionSecurity=measured-uki

[    4.508673] systemd[1]: Starting systemd-remount-fs.service - Remount Root and Kernel File Systems...

[    4.508710] systemd[1]: systemd-tpm2-setup-early.service - Early TPM SRK Setup skipped, unmet condition check ConditionSecurity=measured-uki

[    4.509318] systemd[1]: Starting systemd-udev-load-credentials.service - Load udev Rules from Credentials...

[    4.509914] systemd[1]: Starting systemd-udev-trigger.service - Coldplug All udev Devices...

[    4.511507] systemd[1]: Mounted dev-hugepages.mount - Huge Pages File System.

[    4.511590] systemd[1]: Mounted dev-mqueue.mount - POSIX Message Queue File System.

[    4.511650] systemd[1]: Mounted sys-kernel-debug.mount - Kernel Debug File System.

[    4.511715] systemd[1]: Mounted sys-kernel-tracing.mount - Kernel Trace File System.

[    4.512122] pstore: Using crash dump compression: deflate

[    4.512916] systemd[1]: Finished keyboard-setup.service - Set the console keyboard layout.

[    4.514342] systemd[1]: Mounted proc-sys-fs-binfmt_misc.mount - /proc/sys/fs/binfmt_misc.

[    4.514502] systemd[1]: Finished kmod-static-nodes.service - Create List of Static Device Nodes.

[    4.514565] systemd[1]: Mounted sys-kernel-config.mount - Kernel Configuration File System.

[    4.514610] systemd[1]: Mounted sys-fs-fuse-connections.mount - FUSE Control File System.

[    4.514727] systemd[1]: Finished systemd-modules-load.service - Load Kernel Modules.

[    4.515414] pstore: Registered efi_pstore as persistent store backend

[    4.515550] systemd[1]: Starting systemd-sysctl.service - Apply Kernel Variables...

[    4.516159] systemd[1]: Starting systemd-tmpfiles-setup-dev-early.service - Create Static Device Nodes in /dev gracefully...

[    4.516313] systemd[1]: modprobe@efi_pstore.service: Deactivated successfully.

[    4.516396] systemd[1]: Finished modprobe@efi_pstore.service - Load Kernel Module efi_pstore.

[    4.517310] systemd[1]: Finished systemd-udev-load-credentials.service - Load udev Rules from Credentials.

[    4.520128] systemd-journald[443]: Collecting audit messages is disabled.

[    4.522196] systemd[1]: Finished systemd-sysctl.service - Apply Kernel Variables.

[    4.532201] systemd[1]: Finished systemd-tmpfiles-setup-dev-early.service - Create Static Device Nodes in /dev gracefully.

[    4.536504] EXT4-fs (nvme0n1p2): re-mounted 6640197b-a4e2-4071-9bb1-47aaf3d802ab r/w.

[    4.536959] systemd[1]: Finished systemd-remount-fs.service - Remount Root and Kernel File Systems.

[    4.537415] systemd[1]: systemd-hwdb-update.service - Rebuild Hardware Database skipped, unmet condition check ConditionNeedsUpdate=/etc

[    4.537441] systemd[1]: systemd-pstore.service - Platform Persistent Storage Archival skipped, unmet condition check ConditionDirectoryNotEmpty=/sys/fs/pstore

[    4.537959] systemd[1]: Starting systemd-random-seed.service - Load/Save OS Random Seed...

[    4.537978] systemd[1]: systemd-sysusers.service - Create System Users skipped, no trigger condition checks were met.

[    4.538957] systemd[1]: Starting systemd-journalctl.socket - Journal Log Access Socket...

[    4.539802] systemd[1]: Starting systemd-timesyncd.service - Network Time Synchronization...

[    4.540386] systemd[1]: Starting systemd-tmpfiles-setup-dev.service - Create Static Device Nodes in /dev...

[    4.540405] systemd[1]: systemd-tpm2-setup.service - TPM SRK Setup skipped, unmet condition check ConditionSecurity=measured-uki

[    4.540423] systemd[1]: systemd-pcrnvdone.service - TPM PCR NvPCR Initialization Separator skipped, unmet condition check ConditionSecurity=measured-uki

[    4.540735] systemd[1]: Listening on systemd-journalctl.socket - Journal Log Access Socket.

[    4.544661] systemd[1]: Starting systemd-userdbd.service - User Database Manager...

[    4.544875] systemd[1]: Finished systemd-random-seed.service - Load/Save OS Random Seed.

[    4.547084] systemd[1]: Finished systemd-tmpfiles-setup-dev.service - Create Static Device Nodes in /dev.

[    4.547154] systemd[1]: Reached target local-fs-pre.target - Preparation for Local File Systems.

[    4.547967] systemd[1]: Starting systemd-udevd.service - Rule-based Manager for Device Events and Files...

[    4.549346] systemd[1]: Started systemd-journald.service - Journal Service.

[    4.554995] systemd-journald[443]: Received client request to flush runtime journal.

[    4.738415] ACPI: AC: AC Adapter [AC] (on-line)

[    4.740788] input: Intel HID events as /devices/platform/INTC1051:00/input/input16

[    4.740923] intel-hid INTC1051:00: platform supports 5 button array

[    4.740967] input: Intel HID 5 button array as /devices/platform/INTC1051:00/input/input17

[    4.784321] intel_pmc_core INT33A1:00:  initialized

[    4.835519] EDAC igen6: v2.5.1

[    4.845936] Adding 16513020k swap on /dev/nvme0n1p3.  Priority:-2 extents:1 across:16513020k SS

[    4.909770] mei_me 0000:00:16.0: enabling device (0000 -> 0002)

[    4.969068] mc: Linux media interface: v0.10

[    4.988342] cfg80211: Loading compiled-in X.509 certificates for regulatory database

[    5.001288] Loaded X.509 cert 'benh@debian.org: 577e021cb980e0e820821ba7b54b4961b8b4fadf'

[    5.001538] Loaded X.509 cert 'romain.perier@gmail.com: 3abbc6ec146e09d1b6016ab9d6cf71dd233f0328'

[    5.001761] Loaded X.509 cert 'sforshee: 00b28ddf47aef9cea7'

[    5.001916] Loaded X.509 cert 'wens: 61c038651aabdcf94bd0ac7ff06c7248db18c600'

[    5.045532] videodev: Linux video capture interface: v2.00

[    5.050337] ee1004 0-0050: 512 byte EE1004-compliant SPD EEPROM, read-only

[    5.108776] iwlwifi 0000:00:14.3: enabling device (0000 -> 0002)

[    5.113062] resource: resource sanity check: requesting [mem 0x00000000fedc0000-0x00000000fedcdfff], which spans more than pnp 00:04 [mem 0xfedc0000-0xfedc7fff]

[    5.113069] caller uncore_get_box_mmio_addr+0xe6/0x150 [intel_uncore] mapping multiple BARs

[    5.115795] iwlwifi 0000:00:14.3: Detected crf-id 0x3617, cnv-id 0x20000302 wfpm id 0x80000000

[    5.115814] iwlwifi 0000:00:14.3: PCI dev a0f0/4070, rev=0x351, rfid=0x10a100

[    5.115817] iwlwifi 0000:00:14.3: Detected Intel(R) Wi-Fi 6 AX201 160MHz

[    5.121329] iwlwifi 0000:00:14.3: firmware: failed to load iwl-debug-yoyo.bin (-2)

[    5.121346] iwlwifi 0000:00:14.3: firmware: failed to load iwl-debug-yoyo.bin (-2)

[    5.121358] iwlwifi 0000:00:14.3: firmware: failed to load iwl-debug-yoyo.bin (-2)

[    5.121361] iwlwifi 0000:00:14.3: loaded firmware version 77.f39cc7f9.0 QuZ-a0-hr-b0-77.ucode op_mode iwlmvm

[    5.128797] Bluetooth: Core ver 2.22

[    5.128825] NET: Registered PF_BLUETOOTH protocol family

[    5.128828] Bluetooth: HCI device and connection manager initialized

[    5.128834] Bluetooth: HCI socket layer initialized

[    5.128838] Bluetooth: L2CAP socket layer initialized

[    5.128843] Bluetooth: SCO socket layer initialized

[    5.131757] input: Dell WMI hotkeys as /devices/platform/PNP0C14:02/wmi_bus/wmi_bus-PNP0C14:02/9DBB5994-A997-11DA-B012-B622A1EF5492-8/input/input18

[    5.189812] ACPI: battery: new hook: Dell Primary Battery Extension

[    5.208223] intel_rapl_msr: PL4 support detected.

[    5.208281] intel_rapl_common: Found RAPL domain package

[    5.208286] intel_rapl_common: Found RAPL domain core

[    5.208289] intel_rapl_common: Found RAPL domain uncore

[    5.208292] intel_rapl_common: Found RAPL domain psys

[    5.214837] mei_pxp 0000:00:16.0-fbf6fcf1-96cf-4e2e-a6a6-1bab8cbe36b1: bound 0000:00:02.0 (ops i915_pxp_tee_component_ops [i915])

[    5.215415] mei_hdcp 0000:00:16.0-b638ab7e-94e2-4ea2-a552-d1c54b627f04: bound 0000:00:02.0 (ops i915_hdcp_ops [i915])

[    5.366602] proc_thermal 0000:00:04.0: enabling device (0000 -> 0002)

[    5.374586] RAPL PMU: API unit is 2^-32 Joules, 4 fixed counters, 655360 ms ovfl timer

[    5.374590] RAPL PMU: hw unit of domain pp0-core 2^-14 Joules

[    5.374592] RAPL PMU: hw unit of domain package 2^-14 Joules

[    5.374593] RAPL PMU: hw unit of domain pp1-gpu 2^-14 Joules

[    5.374594] RAPL PMU: hw unit of domain psys 2^-14 Joules

[    5.376697] intel_rapl_common: Found RAPL domain package

[    5.414333] uvcvideo 3-6:1.0: Found UVC 1.00 device Integrated_Webcam_HD (0c45:6a10)

[    5.426265] usbcore: registered new interface driver btusb

[    5.427936] Bluetooth: hci0: Bootloader revision 0.4 build 0 week 30 2018

[    5.431955] Bluetooth: hci0: Device revision is 2

[    5.431960] Bluetooth: hci0: Secure boot is enabled

[    5.431962] Bluetooth: hci0: OTP lock is enabled

[    5.431964] Bluetooth: hci0: API lock is enabled

[    5.431966] Bluetooth: hci0: Debug lock is disabled

[    5.431968] Bluetooth: hci0: Minimum firmware build 1 week 10 2014

[    5.436166] usbcore: registered new interface driver uvcvideo

[    5.441262] Bluetooth: hci0: Found device firmware: intel/ibt-19-0-4.sfi

[    5.441317] Bluetooth: hci0: Boot Address: 0x24800

[    5.441321] Bluetooth: hci0: Firmware Version: 193-33.24

[    5.540895] snd_soc_avs 0000:00:1f.3: Digital mics found on Skylake+ platform, using SOF driver

[    5.625504] loop: module loaded

[    5.632723] loop0: detected capacity change from 0 to 151512

[    5.635942] loop1: detected capacity change from 0 to 136816

[    5.637397] loop2: detected capacity change from 0 to 8

[    5.640122] loop3: detected capacity change from 0 to 187776

[    5.640362] loop4: detected capacity change from 0 to 1241248

[    5.659933] loop5: detected capacity change from 0 to 98104

[    5.661737] squashfs: version 4.0 (2009/01/31) Phillip Lougher

[    5.664188] loop6: detected capacity change from 0 to 2066728

[    5.664459] loop7: detected capacity change from 0 to 808920

[    5.683999] loop8: detected capacity change from 0 to 100888

[    5.839641] iwlwifi 0000:00:14.3: Detected RF HR B3, rfid=0x10a100

[    5.904519] iwlwifi 0000:00:14.3: base HW address: 1c:c1:0c:c2:79:c8

[    5.932879] nvme nvme0: using unchecked data buffer

[    5.978997] sof-audio-pci-intel-tgl 0000:00:1f.3: enabling device (0000 -> 0002)

[    5.979367] sof-audio-pci-intel-tgl 0000:00:1f.3: DSP detected with PCI class/subclass/prog-if 0x040100

[    5.979534] sof-audio-pci-intel-tgl 0000:00:1f.3: bound 0000:00:02.0 (ops intel_audio_component_bind_ops [i915])

[    5.987027] sof-audio-pci-intel-tgl 0000:00:1f.3: use msi interrupt mode

[    6.014215] Bluetooth: BNEP (Ethernet Emulation) ver 1.3

[    6.014221] Bluetooth: BNEP filters: protocol multicast

[    6.014229] Bluetooth: BNEP socket layer initialized

[    6.133509] sof-audio-pci-intel-tgl 0000:00:1f.3: hda codecs found, mask 5

[    6.133520] sof-audio-pci-intel-tgl 0000:00:1f.3: using HDA machine driver skl_hda_dsp_generic now

[    6.133525] sof-audio-pci-intel-tgl 0000:00:1f.3: NHLT device BT(0) detected, ssp_mask 0x4

[    6.133530] sof-audio-pci-intel-tgl 0000:00:1f.3: BT link detected in NHLT tables: 0x4

[    6.133534] sof-audio-pci-intel-tgl 0000:00:1f.3: DMICs detected in NHLT tables: 2

[    6.147563] sof-audio-pci-intel-tgl 0000:00:1f.3: Firmware paths/files for ipc type 0:

[    6.147574] sof-audio-pci-intel-tgl 0000:00:1f.3:  Firmware file:     intel/sof/sof-tgl.ri

[    6.147577] sof-audio-pci-intel-tgl 0000:00:1f.3:  Topology file:     intel/sof-tplg/sof-hda-generic-2ch.tplg

[    6.148839] sof-audio-pci-intel-tgl 0000:00:1f.3: Firmware info: version 2:2:0-57864

[    6.148845] sof-audio-pci-intel-tgl 0000:00:1f.3: Firmware: ABI 3:22:1 Kernel ABI 3:23:1

[    6.260128] sof-audio-pci-intel-tgl 0000:00:1f.3: Firmware info: version 2:2:0-57864

[    6.260136] sof-audio-pci-intel-tgl 0000:00:1f.3: Firmware: ABI 3:22:1 Kernel ABI 3:23:1

[    6.276345] NET: Registered PF_QIPCRTR protocol family

[    6.296025] sof-audio-pci-intel-tgl 0000:00:1f.3: Topology: ABI 3:22:1 Kernel ABI 3:23:1

[    6.296480] skl_hda_dsp_generic skl_hda_dsp_generic: ASoC: Parent card not yet available, widget card binding deferred

[    6.313337] snd_hda_codec_alc269 ehdaudio0D0: ALC3204: picked fixup  (pin match)

[    6.348444] snd_hda_codec_alc269 ehdaudio0D0: autoconfig for ALC3204: line_outs=1 (0x14/0x0/0x0/0x0/0x0) type:speaker

[    6.348453] snd_hda_codec_alc269 ehdaudio0D0:    speaker_outs=0 (0x0/0x0/0x0/0x0/0x0)

[    6.348456] snd_hda_codec_alc269 ehdaudio0D0:    hp_outs=1 (0x21/0x0/0x0/0x0/0x0)

[    6.348458] snd_hda_codec_alc269 ehdaudio0D0:    mono: mono_out=0x0

[    6.348460] snd_hda_codec_alc269 ehdaudio0D0:    inputs:

[    6.348462] snd_hda_codec_alc269 ehdaudio0D0:      Headset Mic=0x19

[    6.348465] snd_hda_codec_alc269 ehdaudio0D0:      Headphone Mic=0x1a

[    6.558160] skl_hda_dsp_generic skl_hda_dsp_generic: hda_dsp_hdmi_build_controls: no PCM in topology for HDMI converter 3

[    6.575396] input: sof-hda-dsp Headphone Mic as /devices/pci0000:00/0000:00:1f.3/skl_hda_dsp_generic/sound/card0/input19

[    6.575468] input: sof-hda-dsp HDMI/DP,pcm=3 as /devices/pci0000:00/0000:00:1f.3/skl_hda_dsp_generic/sound/card0/input20

[    6.575515] input: sof-hda-dsp HDMI/DP,pcm=4 as /devices/pci0000:00/0000:00:1f.3/skl_hda_dsp_generic/sound/card0/input21

[    6.576488] input: sof-hda-dsp HDMI/DP,pcm=5 as /devices/pci0000:00/0000:00:1f.3/skl_hda_dsp_generic/sound/card0/input22

[    6.636935] RPC: Registered named UNIX socket transport module.

[    6.636939] RPC: Registered udp transport module.

[    6.636940] RPC: Registered tcp transport module.

[    6.636941] RPC: Registered tcp-with-tls transport module.

[    6.636941] RPC: Registered tcp NFSv4.1 backchannel transport module.

[    6.814173] audit: type=1400 audit(1780405991.872:2): apparmor="DENIED" operation="change_onexec" class="file" info="label not found" error=-2 profile="unconfined" name="snap-update-ns.cups" pid=1050 comm="snap-confine"

[    6.816786] audit: type=1400 audit(1780405991.876:3): apparmor="DENIED" operation="change_onexec" class="file" info="label not found" error=-2 profile="unconfined" name="snap-update-ns.cups" pid=1054 comm="snap-confine"

[    7.231128] audit: type=1400 audit(1780405992.288:4): apparmor="DENIED" operation="change_onexec" class="file" info="label not found" error=-2 profile="unconfined" name="snap-update-ns.cups" pid=1114 comm="snap-confine"

[    7.238425] audit: type=1400 audit(1780405992.296:5): apparmor="DENIED" operation="change_onexec" class="file" info="label not found" error=-2 profile="unconfined" name="snap-update-ns.cups" pid=1117 comm="snap-confine"

[    7.400566] Bluetooth: hci0: Waiting for firmware download to complete

[    7.401578] Bluetooth: hci0: Firmware loaded in 1914365 usecs

[    7.401642] Bluetooth: hci0: Waiting for device to boot

[    7.416689] Bluetooth: hci0: Device booted in 14708 usecs

[    7.417114] Bluetooth: hci0: Found Intel DDC parameters: intel/ibt-19-0-4.ddc

[    7.418600] Bluetooth: hci0: Applying Intel DDC parameters completed

[    7.419597] Bluetooth: hci0: Firmware revision 0.4 build 193 week 33 2024

[    7.421616] Bluetooth: hci0: HCI LE Coded PHY feature bit is set, but its usage is not supported.

[    7.484801] Bluetooth: MGMT ver 1.23

[    7.491896] NET: Registered PF_ALG protocol family

[    7.523937] Bluetooth: RFCOMM TTY layer initialized

[    7.523948] Bluetooth: RFCOMM socket layer initialized

[    7.523953] Bluetooth: RFCOMM ver 1.11

[    7.578428] audit: type=1400 audit(1780405992.636:6): apparmor="DENIED" operation="change_onexec" class="file" info="label not found" error=-2 profile="unconfined" name="snap-update-ns.cups" pid=1163 comm="snap-confine"

[    7.580506] audit: type=1400 audit(1780405992.640:7): apparmor="DENIED" operation="change_onexec" class="file" info="label not found" error=-2 profile="unconfined" name="snap-update-ns.cups" pid=1165 comm="snap-confine"

[    8.021148] audit: type=1400 audit(1780405993.080:8): apparmor="DENIED" operation="change_onexec" class="file" info="label not found" error=-2 profile="unconfined" name="snap-update-ns.cups" pid=1216 comm="snap-confine"

[    8.027159] audit: type=1400 audit(1780405993.084:9): apparmor="DENIED" operation="change_onexec" class="file" info="label not found" error=-2 profile="unconfined" name="snap-update-ns.cups" pid=1219 comm="snap-confine"

[    8.249983] audit: type=1400 audit(1780405993.308:10): apparmor="DENIED" operation="change_onexec" class="file" info="label not found" error=-2 profile="unconfined" name="snap-update-ns.cups" pid=1271 comm="snap-confine"

[    8.261366] audit: type=1400 audit(1780405993.320:11): apparmor="DENIED" operation="change_onexec" class="file" info="label not found" error=-2 profile="unconfined" name="snap-update-ns.cups" pid=1275 comm="snap-confine"

[    9.386796] wlan0: authenticate with f4:e8:4f:f0:f7:b9 (local address=1c:c1:0c:c2:79:c8)

[    9.387674] wlan0: send auth to f4:e8:4f:f0:f7:b9 (try 1/3)

[    9.549676] wlan0: authenticate with f4:e8:4f:f0:f7:b9 (local address=1c:c1:0c:c2:79:c8)

[    9.549685] wlan0: send auth to f4:e8:4f:f0:f7:b9 (try 1/3)

[    9.550568] wlan0: authenticated

[    9.555931] wlan0: associate with f4:e8:4f:f0:f7:b9 (try 1/3)

[    9.559653] wlan0: RX AssocResp from f4:e8:4f:f0:f7:b9 (capab=0x1931 status=0 aid=16)

[    9.564850] wlan0: associated

[    9.608269] iwlwifi 0000:00:14.3: Unhandled alg: 0x707

[    9.629501] wlan0: Limiting TX power to 30 (30 - 0) dBm as advertised by f4:e8:4f:f0:f7:b9

[   10.098057] evm: overlay not supported

[   10.161891] Initializing XFRM netlink socket

[   10.470197] bridge: filtering via arp/ip/ip6tables is no longer available by default. Update your scripts to load br_netfilter if you need this.

[   10.951609] br-abf08b18fc99: port 1(veth39abbd3) entered blocking state

[   10.951616] br-abf08b18fc99: port 1(veth39abbd3) entered disabled state

[   10.951623] veth39abbd3: entered allmulticast mode

[   10.951702] veth39abbd3: entered promiscuous mode

[   10.983835] eth0: renamed from veth75887d4

[   10.984291] br-abf08b18fc99: port 1(veth39abbd3) entered blocking state

[   10.984296] br-abf08b18fc99: port 1(veth39abbd3) entered forwarding state

[   22.034839] block nvme0n1: No UUID available providing old NGUID

[   57.402302] warning: `ThreadPoolForeg' uses wireless extensions which will stop working for Wi-Fi 7 hardware; use nl80211

[ 3706.611267] perf: interrupt took too long (2518 > 2500), lowering kernel.perf_event_max_sample_rate to 79250

[ 8318.559291] perf: interrupt took too long (3149 > 3147), lowering kernel.perf_event_max_sample_rate to 63500

[ 9881.092265] perf: interrupt took too long (3937 > 3936), lowering kernel.perf_event_max_sample_rate to 50750

[28338.397289] usb 3-7: new high-speed USB device number 6 using xhci_hcd

[28338.566478] usb 3-7: New USB device found, idVendor=0bda, idProduct=0177, bcdDevice=77.11

[28338.566490] usb 3-7: New USB device strings: Mfr=1, Product=2, SerialNumber=3

[28338.566494] usb 3-7: Product: USB2.0-CRW

[28338.566497] usb 3-7: Manufacturer: Generic

[28338.566500] usb 3-7: SerialNumber: 20121112761000000

[28338.627121] usbcore: registered new interface driver usb-storage

[28338.631379] usbcore: registered new interface driver uas

[28338.635019] ums-realtek 3-7:1.0: USB Mass Storage device detected

[28338.647474] scsi host0: usb-storage 3-7:1.0

[28338.647597] usbcore: registered new interface driver ums-realtek

[28339.680345] scsi 0:0:0:0: Direct-Access     Generic- SD/MMC/MS PRO    1.00 PQ: 0 ANSI: 4

[28339.702957] scsi 0:0:0:0: Attached scsi generic sg0 type 0

[28340.684080] sd 0:0:0:0: [sda] 62309376 512-byte logical blocks: (31.9 GB/29.7 GiB)

[28340.684520] sd 0:0:0:0: [sda] Write Protect is off

[28340.684528] sd 0:0:0:0: [sda] Mode Sense: 2f 00 00 00

[28340.684863] sd 0:0:0:0: [sda] Write cache: disabled, read cache: enabled, doesn't support DPO or FUA

[28340.820298]  sda: sda1

[28340.820596] sd 0:0:0:0: [sda] Attached SCSI removable disk

[28577.597006] usb 4-2: new SuperSpeed USB device number 2 using xhci_hcd

[28577.617347] usb 4-2: New USB device found, idVendor=0951, idProduct=1666, bcdDevice= 1.00

[28577.617358] usb 4-2: New USB device strings: Mfr=1, Product=2, SerialNumber=3

[28577.617362] usb 4-2: Product: DataTraveler 3.0

[28577.617366] usb 4-2: Manufacturer: Kingston

[28577.617369] usb 4-2: SerialNumber: E0D55EA52348E8C128AC0A33

[28577.623684] usb-storage 4-2:1.0: USB Mass Storage device detected

[28577.623795] scsi host1: usb-storage 4-2:1.0

[28578.636095] scsi 1:0:0:0: Direct-Access     Kingston DataTraveler 3.0 PMAP PQ: 0 ANSI: 6

[28578.636676] sd 1:0:0:0: Attached scsi generic sg1 type 0

[28579.778501] sd 1:0:0:0: [sdb] 241778880 512-byte logical blocks: (124 GB/115 GiB)

[28579.778984] sd 1:0:0:0: [sdb] Write Protect is off

[28579.778987] sd 1:0:0:0: [sdb] Mode Sense: 2b 00 00 08

[28579.779181] sd 1:0:0:0: [sdb] Write cache: disabled, read cache: enabled, doesn't support DPO or FUA

[28579.822137]  sdb:

[28579.822170] sd 1:0:0:0: [sdb] Attached SCSI removable disk

[28584.708942] usb 4-2: USB disconnect, device number 2

[28586.309631] usb 3-1: USB disconnect, device number 2

[28590.941057] usb 4-1: new SuperSpeed USB device number 3 using xhci_hcd

[28590.961492] usb 4-1: New USB device found, idVendor=0951, idProduct=1666, bcdDevice= 1.00

[28590.961505] usb 4-1: New USB device strings: Mfr=1, Product=2, SerialNumber=3

[28590.961508] usb 4-1: Product: DataTraveler 3.0

[28590.961512] usb 4-1: Manufacturer: Kingston

[28590.961514] usb 4-1: SerialNumber: E0D55EA52348E8C128AC0A33

[28590.963684] usb-storage 4-1:1.0: USB Mass Storage device detected

[28590.964260] scsi host1: usb-storage 4-1:1.0

[28591.979901] scsi 1:0:0:0: Direct-Access     Kingston DataTraveler 3.0 PMAP PQ: 0 ANSI: 6

[28591.980457] sd 1:0:0:0: Attached scsi generic sg1 type 0

[28593.125472] sd 1:0:0:0: [sdb] 241778880 512-byte logical blocks: (124 GB/115 GiB)

[28593.126381] sd 1:0:0:0: [sdb] Write Protect is off

[28593.126387] sd 1:0:0:0: [sdb] Mode Sense: 2b 00 00 08

[28593.126886] sd 1:0:0:0: [sdb] Write cache: disabled, read cache: enabled, doesn't support DPO or FUA

[28593.162675]  sdb:

[28593.162722] sd 1:0:0:0: [sdb] Attached SCSI removable disk

[28593.784933] usb 4-1: USB disconnect, device number 3

[28594.416953] usb 3-1: new high-speed USB device number 7 using xhci_hcd

[28595.468982] usb 4-1: new SuperSpeed USB device number 4 using xhci_hcd

[28595.489095] usb 4-1: New USB device found, idVendor=0951, idProduct=1666, bcdDevice= 1.00

[28595.489106] usb 4-1: New USB device strings: Mfr=1, Product=2, SerialNumber=3

[28595.489110] usb 4-1: Product: DataTraveler 3.0

[28595.489114] usb 4-1: Manufacturer: Kingston

[28595.489117] usb 4-1: SerialNumber: E0D55EA52348E8C128AC0A33

[28595.491153] usb-storage 4-1:1.0: USB Mass Storage device detected

[28595.491815] scsi host1: usb-storage 4-1:1.0

[28596.523953] scsi 1:0:0:0: Direct-Access     Kingston DataTraveler 3.0 PMAP PQ: 0 ANSI: 6

[28596.524460] sd 1:0:0:0: Attached scsi generic sg1 type 0

[28597.669137] sd 1:0:0:0: [sdb] 241778880 512-byte logical blocks: (124 GB/115 GiB)

[28597.670113] sd 1:0:0:0: [sdb] Write Protect is off

[28597.670122] sd 1:0:0:0: [sdb] Mode Sense: 2b 00 00 08

[28597.670637] sd 1:0:0:0: [sdb] Write cache: disabled, read cache: enabled, doesn't support DPO or FUA

[28597.722703]  sdb:

[28597.722783] sd 1:0:0:0: [sdb] Attached SCSI removable disk

[28599.164934] usb 4-1: USB disconnect, device number 4

[28600.512974] usb 4-1: new SuperSpeed USB device number 5 using xhci_hcd

[28600.533277] usb 4-1: New USB device found, idVendor=0951, idProduct=1666, bcdDevice= 1.00

[28600.533288] usb 4-1: New USB device strings: Mfr=1, Product=2, SerialNumber=3

[28600.533292] usb 4-1: Product: DataTraveler 3.0

[28600.533296] usb 4-1: Manufacturer: Kingston

[28600.533298] usb 4-1: SerialNumber: E0D55EA52348E8C128AC0A33

[28600.535440] usb-storage 4-1:1.0: USB Mass Storage device detected

[28600.536125] scsi host1: usb-storage 4-1:1.0

[28601.464986] usb 4-1: USB disconnect, device number 5

[28605.440981] usb 4-1: new SuperSpeed USB device number 6 using xhci_hcd

[28605.461145] usb 4-1: New USB device found, idVendor=0951, idProduct=1666, bcdDevice= 1.00

[28605.461157] usb 4-1: New USB device strings: Mfr=1, Product=2, SerialNumber=3

[28605.461161] usb 4-1: Product: DataTraveler 3.0

[28605.461164] usb 4-1: Manufacturer: Kingston

[28605.461166] usb 4-1: SerialNumber: E0D55EA52348E8C128AC0A33

[28605.463196] usb-storage 4-1:1.0: USB Mass Storage device detected

[28605.463728] scsi host1: usb-storage 4-1:1.0

[28606.478938] scsi 1:0:0:0: Direct-Access     Kingston DataTraveler 3.0 PMAP PQ: 0 ANSI: 6

[28606.479335] sd 1:0:0:0: Attached scsi generic sg1 type 0

[28607.624716] sd 1:0:0:0: [sdb] 241778880 512-byte logical blocks: (124 GB/115 GiB)

[28607.625526] sd 1:0:0:0: [sdb] Write Protect is off

[28607.625533] sd 1:0:0:0: [sdb] Mode Sense: 2b 00 00 08

[28607.625865] sd 1:0:0:0: [sdb] Write cache: disabled, read cache: enabled, doesn't support DPO or FUA

[28607.678084]  sdb:

[28607.678119] sd 1:0:0:0: [sdb] Attached SCSI removable disk

^C



~ 

❯ ls /dev/sd*

󰡯 /dev/sda  󰡯 /dev/sda1  󰡯 /dev/sdb



~ 

❯ sudo mkdir -p /mnt/usb

sudo mount /dev/sdb1 /mnt/usb

mount: /mnt/usb: fsconfig() failed: /dev/sdb1: Can't lookup blockdev.

       dmesg(1) may have more information after failed mount system call.



~ 

❯ ls -lah /mnt/usb



~ 

❯ 
