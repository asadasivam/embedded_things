Driver flow

```text
Bash / user program
      ↓
system call
      ↓
kernel core
      ↓
device driver
      ↓
hardware
      ↓
device driver finishes / waits
      ↓
kernel core
      ↓
system call returns
      ↓
user program / Bash continues
```

Example

```text
echo program
  calls write()
      ↓
Linux kernel receives write syscall
      ↓
kernel finds driver for /dev/ttyUSB0
      ↓
USB/UART driver sends data
      ↓
driver returns status to kernel
      ↓
kernel returns result to echo program
      ↓
echo exits
      ↓
bash shows prompt again
```
