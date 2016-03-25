# scaleway-ipxe
:dancer: custom IPXE config on Scaleway servers

## Usage

```console
$ scw-ipxe.expect "50G" "chain --autofree http://boot.netboot.xyz/menu.ipxe"

```

```console
$ scw-ipxe.expect "50G" "initrd http://ftp.ch.openbsd.org/pub/OpenBSD/5.8/amd64/install58.iso" "chain http://boot.salstar.sk/memdisk iso raw"

```

## License

MIT
