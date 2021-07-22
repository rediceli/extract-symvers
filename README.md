# extract-symvers.py

Extract `Module.symvers` from kernel binary.

## Usage

```
python extract-symvers.py -B/--base-address <load_addr> -e/--endian <big|be|little|le> -b/--bits <32|64>
```

  - -B/--base-address: Kernel load address
  - -e/--endian: Kernel endian (default little endian)
  - -b/--bits: Kernel bits, 32 for i386/arm, 64 for x86_64/aarch64 etc

## Example

For 32bit kernel:

```
python extract-symvers.py -B {KERNEL_LOAD_ADDR} -b 32 ./kernel.bin
```

For 64bit kernel:
```
python extract-symvers.py -B {KERNEL_LOAD_ADDR} -b 64 ./kernel.bin
```

