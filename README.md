# FreeRTOS-RISC-V-RV32

## Prerequisites

* Toolchain

## Build

```
$ cd FreeRTOS/Demo/RISC-V_RV32_QEMU_VIRT_GCC
$ make -C build/gcc/
```

## Run

To run the image in QEMU, use the following command:

```
$ qemu-system-riscv32 -nographic -machine virt -net none \
    -chardev stdio,id=con,mux=on -serial chardev:con \
    -mon chardev=con,mode=readline -bios none \
    -smp 4 -kernel ./build/gcc/output/RTOSDemo.elf
```
