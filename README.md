# Hackintosh-ASUS-TUF-GAMING-B650M-PLUS-WIFI-7800X3D-RX-6900-XT


# Target macOS and status

Target Version: macOS Sonoma 14.4 + macOS Ventura 13.7.6

OpenCore Version: 1.0.5

**Current status: Installation is working :D and Sonoma is running**
- WiFi + BT is not working!

# Hardware Information

- CPU: AMD Ryzen 7 7800X3D 8-Core Processor
- Board: ASUS TUF Gaming B650M-Plus WiFi
- - BIOS Version: 2.22.1284
- RAM: Corsair Vengeance black DIMM Kit 32GB, DDR5-6000, CL30-36-36-76
- GPU: PowerColor RX 6900 XT Red Devil Ultimate // Navi 21 XTXH (PCI Express 4.0 x16 1002 / 73AF, Rev C0)
- SSD: ADATA XPG Gammix S11 Pro 1TB PCIe 4.0 NVMe M.2

<details>
<summary>OCSysInfo</summary>

```sh
─ CPU
  └── AMD Ryzen 7 7800X3D 8-Core Processor           
      ├── Cores: 8
      ├── Threads: 16
      ├── SSE: SSE4.2
      ├── SSSE3: Supported
      └── Codename: Zen 4

─ Motherboard
  ├── Model: TUF GAMING B650M-PLUS WIFI
  ├── Manufacturer: ASUSTeK COMPUTER INC.
  └── BIOS: 2413 (2024/02/07)

─ GPU
  ├── AMD Radeon RX 6900 XT
  │   ├── Device ID: 0x73AF
  │   ├── Vendor: 0x1002
  │   ├── PCI Path: PciRoot(0x0)/Pci(0x1,0x1)/Pci(0x0,0x0)/Pci(0x0,0x0)/Pci(0x0,0x0)
  │   ├── ACPI Path: \_SB.PCI0.GPP0.SWUS.SWDS.VGA_
  │   └── Codename: Sienna Cichlid
  └── AMD Radeon(TM) Graphics
      ├── Device ID: 0x164E
      ├── Vendor: 0x1002
      ├── PCI Path: PciRoot(0x0)/Pci(0x8,0x1)/Pci(0x0,0x0)
      └── ACPI Path: \_SB.PCI0.GP17.VGA_

─ Memory
  ├── CMK32GX5M2B6000C30 (Part-Number)
  │   ├── Type: Unknown
  │   ├── Slot
  │   │   ├── Bank: P0 CHANNEL A
  │   │   └── Channel: DIMM 1
  │   ├── Frequency (MHz): 6000 MHz
  │   ├── Manufacturer: Corsair
  │   └── Capacity: 16384MB
  └── CMK32GX5M2B6000C30 (Part-Number)
      ├── Type: Unknown
      ├── Slot
      │   ├── Bank: P0 CHANNEL B
      │   └── Channel: DIMM 1
      ├── Frequency (MHz): 6000 MHz
      ├── Manufacturer: Corsair
      └── Capacity: 16384MB

─ Network
  └── RTL8125 2.5GbE Controller
      ├── Device ID: 0x8125
      ├── Vendor: 0x10EC
      ├── PCI Path: PciRoot(0x0)/Pci(0x2,0x1)/Pci(0x0,0x0)/Pci(0xa,0x0)/Pci(0x0,0x0)
      └── ACPI Path: \_SB.PCI0.GPP7.UP00.DP50.EP00

─ Audio
  ├── RV635 HDMI Audio [Radeon HD 3650/3730/3750]
  │   ├── Device ID: 0xAA01
  │   └── Vendor: 0x1002
  ├── Unknown Sound Device
  │   ├── Device ID: 0x020E
  │   └── Vendor: 0xBE57
  ├── RV635 HDMI Audio [Radeon HD 3650/3730/3750]
  │   ├── Device ID: 0xAA01
  │   └── Vendor: 0x1002
  ├── Realtek ALC897
  │   ├── Device ID: 0x0897
  │   └── Vendor: 0x10EC
  └── Unknown Sound Device
      ├── Device ID: 0x0100
      └── Vendor: 0x2F96

─ Input
  ├── HID Keyboard Device
  │   ├── Product ID: 0xC547
  │   └── Vendor ID: 0x046D
  ├── USB Input Device (USB)
  │   ├── Product ID: 0x0081
  │   └── Vendor ID: 0x3299
  ├── HID Keyboard Device
  │   ├── Product ID: 0x0081
  │   └── Vendor ID: 0x3299
  ├── USB Input Device (USB)
  │   ├── Product ID: 0xC547
  │   └── Vendor ID: 0x046D
  └── HID-compliant mouse
      ├── Product ID: 0x0081
      └── Vendor ID: 0x3299

─ Storage
  └── Samsung 980 PRO 1000GB
      ├── Type: NVMe
      ├── Connector: PCI Express
      └── Location: Internal
```

</details>

<br/>

# BIOS Settings

<details>
<summary>BIOS Settings</summary>

## Boot / Secure Boot
- Secure boot state: **User**
- OS Type: **Other OS**
- Secure Boot Mode: **Custom**

## RAM Settings
- **DOCP I / EXPO / XMP  loaded**
    - DDR5-6000 30-36-36-76-2N-1.4
## CPU Configuration
- PSS Support: Enabled
- NX Mode: Enabled
- SVM Mode: Enabled
## PCI Subsystem Settings
- Above 4G Decoding: **Enabled**
- Resize BAR Support: **Enabled**
- SR-IOV Support: Disabled
## USB Configuration
- Legacy USB Support: Enabled
- XHCI Hand-off: Enabled
- USB Mass Storage Driver Support: Disabled

## Onboard Devices Configuration / Serial Port Configuration
- Serial Port: **Disabled**

## NB Configuration
- Primary Video Device: PCIE Video
- Integrated Graphics: **Disabled**

</details>

## Tweaks
Discord: Install AMDfriend and run the following command:
```console
./amdfriend --in-place --sign ~/Library/Application\ Support/discord/0.0.*/modules/discord_krisp/discord_krisp.node
```

WoW Stutter:
Check the refresh rate of the main display, in my case 120 Hz is wokring great while 174,88 Hz is causing stutter.

## Application Slide Values for memmap.txt:
```sh
1363.08 MB @ 0x0B021000: slide=88
  154.0 MB @   0x100000: slide=0
  13.44 MB @ 0x0A290000: slide=81
    2.0 MB @ 0x0A000000: slide=80
```

## Using DevirtualiseMmio from logfile

```sh
15:751 00:002 OCABC: MMIO devirt start
15:753 00:002 OCABC: MMIO devirt 0xE0000000 (0x10000 pages, 0x800000000000100D) skip 0
15:756 00:002 OCABC: MMIO devirt 0xF7000000 (0x7E00 pages, 0x800000000000100D) skip 0
15:758 00:002 OCABC: MMIO devirt 0xFEE00000 (0x1 pages, 0x8000000000000001) skip 0
15:761 00:002 OCABC: MMIO devirt 0xFEE01000 (0x11FF pages, 0x800000000000100D) skip 0
15:763 00:002 OCABC: MMIO devirt 0x880000000 (0x20200 pages, 0x800000000000100D) skip 0
15:765 00:002 OCABC: MMIO devirt end, saved 935936 KB
15:768 00:002 OCABC: Only 168/256 slide values are usable!
15:770 00:002 OCABC: Valid slides - 88-255
```

### Converting to decimal
```sh
0xE0000000    ---> 3758096384
0xF7000000    ---> 4143972352
0xFEE00000    ---> 4276092928
0xFEE01000    ---> 4276097024
0x880000000   ---> 36507222016
```
