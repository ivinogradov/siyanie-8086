# siyanie-8086
C/NASM RTOS for 8086 architecture

(c) Ilya Vinogradov, 2010

Siyanie RTOS is a my attempt to port my RTOS academic project to boot from the floppy disk and run on a real hardware instead of the emulator. The copiled binary occupies the first 512 bytes of the floppy disk and loads in real mode from the floppy disk when a PC boots. It doesn't switch to the protected mode on purpose so that it can work on all CPU of x86 family starting with 8086. After it boots, it attempts to write into interrupt vector table (IVT) to attach keybord interrupt handler to a particular interrupts so the keystrokes can interrupt the simple task it runs.
It also implements the context switching between several tasks that are running.
