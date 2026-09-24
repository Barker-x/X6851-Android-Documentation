# Infinix X6851 Partition Information

Partition information collected from the Infinix Note 40 Pro 5G (X6851) during Android and fastboot testing.

## Dynamic Partitions

The X6851 uses a `super` partition for dynamic Android partitions.

The device reports:

```text
super-partition-name: super
```

The following logical partitions have been observed:

| Partition    | Observed Size |
| ------------ | ------------: |
| system_a     |    0xD6D1C000 |
| system_ext_a |    0x6FEE6000 |
| vendor_a     |    0x2C045000 |

Other logical partitions observed during firmware extraction/testing include:

* `product`
* `odm`
* `system`
* `system_ext`
* `vendor`

## Boot-related Partitions

The device exposes the following boot-related partitions:

* `boot_a`
* `boot_b`
* `init_boot_a`
* `init_boot_b`
* `vendor_boot_a`

The device uses an A/B partition configuration.

## Firmware Payload

XOS 16 firmware was distributed using `payload.bin`.

The payload contained images including:

* `boot`
* `dtbo`
* `odm`
* `product`
* `system`
* `system_ext`
* `vendor`
* `vendor_boot`

The extracted payload did not contain a `super.img`; the Android logical partitions are handled through the device's `super` partition.

## Notes

Partition sizes and availability may differ between firmware versions.

Values documented here are observations from X6851 testing and should be verified against the specific firmware version being used.
