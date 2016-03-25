# scaleway-ipxe
:dancer: custom IPXE config on Scaleway servers

## Usage

```console
$ scw-ipxe.expect "50G" "chain --autofree http://boot.netboot.xyz/menu.ipxe"
spawn slow-stream --raw -b 1 -i 10 --stdout-passthrough -- scw run --attach 50G
You are connected, type 'Ctrl+q' to quit.
Google, Inc.
Serial Graphics Adapter 12/07/13
SGABIOS $Id: sgabios.S 8 2010-04-22 00:03:40Z nlaredo $ (buildd@allspice) Sat Dec  7 23:13:17 UTC 2013
Term: 80x24
SeaBIOS (version Ubuntu-1.8.2-1~ppa3)
iPXE (http://ipxe.org) 00:02.0 C100 PCI2.10 PnP PMM+7FF90B00+7FEF0B00 C100
Booting from ROM...
iPXE (PCI 00:02.0) starting execution...ok
iPXE initialising devices...ok
iPXE 1.0.0+git-20131111.c3d1e78-2ubuntu1.1 -- Open Source Network Boot Firmware -- hhttttpp::////iippxxee..oorrgg
Features: HTTP HTTPS iSCSI DNS TFTP AoE bzImage ELF MBOOT PXE PXEXT Menu

iPXE> dhcp
Configuring (net0 de:19:44:06:a0:0e)...... ok
iPXE> chain --autofree http://boot.netboot.xyz/menu.ipxe
http://boot.netboot.xyz/menu.ipxe......... ok
boot.cfg... ok

Updated version of netboot.xyz is available:

Running version.....1.0.0+git-20131111.c3d1e78-2ubuntu1.1
Updated version.....1.04

Please download the latest version from netboot.xyz.

Attempting to chain to latest version...
http://boot.netboot.xyz/ipxe/netboot.xyz-undionly.kpxe... ok
PXE->EB: !PXE at 9C36:0720, entry point at 9C36:0316
         UNDI code segment 9C36:07BD, data segment 9CB2:2CD8 (624-638kB)
         UNDI device is PCI 00:02.0, type DIX+802.3
         624kB free base memory after PXE unload
iPXE initialising devices...ok

iPXE 1.0.0+ (f8e1) -- Open Source Network Boot Firmware -- http://ipxe.org
Features: DNS HTTP HTTPS iSCSI TFTP VLAN AoE ELF MBOOT PXE bzImage COMBOOT Menu PXEXT
netboot.xyz v1.04
Configuring (net0 de:19:44:06:a0:0e)............... ok
https://boot.netboot.xyz/menu.ipxe...... ok
boot.cfg... ok

                                boot.netboot.xyz

   Default:
      Boot from local hdd
   Installers:
      Linux Installers
      BSD Installers
      FreeDOS Installers
      Hypervisor Installers
   Tools:
      Utilities
      iPXE shell
      Network card info
      netboot.xyz Signature Checks [ enabled: true ]
      Image Signature Checks [ enabled: true ]
```

```console
$ scw-ipxe.expect "50G" "initrd http://ftp.ch.openbsd.org/pub/OpenBSD/5.8/amd64/install58.iso" "chain http://boot.salstar.sk/memdisk iso raw"

```

## License

MIT
