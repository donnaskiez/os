 nasm -felf32 boot/boot.asm -o boot/boot.o

/home/user/donna/Toolchain/i686-elf/bin/i686-elf-gcc -c kernel/main.c -o kernel/kernel.o -std=gnu99 -ffreestanding -O2 -Wall -Wextra

/home/user/donna/Toolchain/i686-elf/bin/i686-elf-gcc -T linker.ld -o os.bin -ffreestanding -O2 -nostdlib boot/boot.o kernel/kernel.o -lgcc

qemu-system-i386 -kernel os.bin