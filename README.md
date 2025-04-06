# Getting Started

## Initialization

```bash
west init -m git@github.com:manojkumarpaladugu/STM32-Zephyr --mr main zephyr-ws
cd zephyr-ws
west update
```

## Build and running

To build the application,

```bash
west build -d _out/ast1030 --pristine -b ast1030_evb STM32-Zephyr/app/
```

To run the application,

```bash
qemu-system-arm -machine ast1030-evb -cpu cortex-m4 -nographic -kernel /workspaces/zephyr-ws/_out/ast1030/zephyr/zephyr.elf
```

To terminate QEMU, press Ctrl + A followed by X
