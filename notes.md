### BP5 Make and build files

Create a build directory and navigate to it:

```bash
$ mkdir build && cd build
$ cmake ..
$ make -j$(nproc)
```


### RPI2040 Firmware flashing with J-Link

```bash
$ sudo openocd -f tcl/interface/jlink.cfg -f tcl/target/rp2040.cfg -c "adapter speed 6000"

$ openocd -f tcl/interface/jlink.cfg -c "transport select swd" -c "adapter_khz 6000" -f tcl/target/rp2040.cfg  -c "program buspiratev.elf reset exit"
```
