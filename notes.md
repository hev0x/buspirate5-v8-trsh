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
```
