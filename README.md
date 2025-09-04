Demo project with box2d for sc6531/sc6530 feature phones based on [fpdoom by ilyakurdyukov](https://github.com/ilyakurdyukov/fpdoom)

https://github.com/user-attachments/assets/ef7982e9-9a7d-40c0-82c6-0f86168678dd

# Build
**!!! Don't forget to clone recursively**
- ```make -C fpdoom/pack_reloc/```
- ```TOOLCHAIN=/usr/bin/arm-none-eabi make```

# Run
- Compile all necessary binaries (`libc_server`  `nor_fdl1.bin`  `spd_dump`) or just download them from fpdoom releases, put them into `workdir`
- `cd workdir`
- `./run.sh`

# VSCode
- Install clangd extension
- Generate compile_commands.json:
```make clean && TOOLCHAIN=/usr/bin/arm-none-eabi bear -- make```
- Ctrl+Shift+B to run on the phone in flash mode connected with usb
