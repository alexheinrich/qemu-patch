# Steps to create patch
Make the defconfig for qemu-system-aarch64:
```
make qemu_aarch64_virt_defconfig
```

Build it:
```
make
```

Check if host-qemu is installed:
```
make menuconfig
```
and search for qemu.


Assuming it is, if you want to recompile after changes run:
```
make host-qemu-rebuild
```

Then run the modified build script in `output/images/start-qemu.sh`.
There should now be both a `ttyAMA0` and `ttyAMA1` device in the vm.
