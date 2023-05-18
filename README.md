# raspi0-qemu
scripts to boot a Raspberry Pi OS image on its native kernel and dtb with QEMU

# Raspberry Pi OS image preparation

Download the newest Raspberry Pi OS image: <br />
https://downloads.raspberrypi.org/raspios_lite_armhf/images/raspios_lite_armhf-2023-05-03/2023-05-03-raspios-bullseye-armhf-lite.img.xz

Decompress the image: <br />
``xz --decompress raspios_lite_armhf-2023-05-03/2023-05-03-raspios-bullseye-armhf-lite.img.xz --verbose``

Resize the image to base-2: <br />
``qemu-img resize -f raw raspios_lite_armhf-2023-05-03/2023-05-03-raspios-bullseye-armhf-lite.img 4096M``

Rename the image: <br />
``mv raspios_lite_armhf-2023-05-03/2023-05-03-raspios-bullseye-armhf-lite.img -v pi.img``

# Kernel and DTB
I copied the DTB and kernel from one of my Raspberry Pi Zero W

I updated the Pi Zero's software and firmware before copying the kernel and DTB: <br />
``sudo apt update
sudo apt upgrade -y

sudo rpi-update

sudo reboot``
