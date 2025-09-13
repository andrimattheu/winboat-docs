# Get Started with WinBoat

Welcome to the WinBoat documentation! This guide will help you get started with installing and using WinBoat to run Windows applications seamlessly on your Linux system.

## Installation
### Available builds
WinBoat offers several builds to suit different needs. Make sure to choose the one that best fits your requirements.
- **AppImage**: A portable version that can run on most Linux distributions without installation.
- **.deb**: Suitable for Debian-based distributions like Ubuntu.
- **.rpm**: Suitable for Red Hat-based distributions like Fedora.

Once you have selected the appropriate build, download it from the [releases page](https://www.winboat.app#downloads). The installation files will carefully guide you through the setup process.

## Setup

**Make sure you have the following prerequisites:**
- At least 4GB of RAM
- At least 2 CPU threads
- At least 32GB of free disk space
- Virtualization (KVM) enabled in your BIOS/UEFI settings | [How to enable KVM?](./guides/enable-kvm.html)
- Docker installed on your system | [How to install Docker?](https://docs.docker.com/get-started/get-docker/)
- Docker Compose v2 installerd on your system | [How to install Docker Compose v2?](https://docs.docker.com/compose/install/)
- User added to the `docker` group | [How to add user to docker group?](https://docs.docker.com/engine/install/linux-postinstall/#manage-docker-as-a-non-root-user)
- FreeRDP client installed on your system | [How to install FreeRDP?](https://www.freerdp.com/)
- `iptables` and `iptable_nat` modules loaded in your kernel | [How to load iptables modules?](https://wiki.archlinux.org/title/Iptables#Loading_kernel_modules)

Once you have ensured that all prerequisites are met, launch WinBoat. These prerequisities will also be checked by the application itself. After accepting the License Agreement, you will be guided through the VM creation process, where you can specify your preferences and configurations.

The ISO files are downloaded automatically by WinBoat, so you don't need to worry about finding them yourself. Right now, only official Microsoft ISOs are supported which are requested from the Microsoft servers. Using custom ISOs is not supported at the moment - you may still attempt to use them but we are unable to provide support for any issues that may arise from doing so.