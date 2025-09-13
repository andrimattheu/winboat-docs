# Frequently Asked Questions

## How does it compare to WinApps?
With WinApps you do the bulk of the setup manually, and there's no cohesive interface to bring it all together. There's a basic TUI, a taskbar widget, and some CLI commands for you to play with.

WinBoat does all the setup once you have the pre-requisites installed, displays everything worth seeing in a neat interface for you, and acts like a complete experience. No need to mess with configuration files, no need to memorize a dozen CLI commands, it just works.

## What are the advantages of using this over CrossOver or WINE?
You can run stuff that doesn't play well with CrossOver or WINE, and have a full Windows desktop at the same time.

We've had numerous apps that weren't working nicely (or at all) in Wine, this is one of the reasons we've created WinBoat. Some examples would be Affinity Photo, Paint Tool Sai v1.0, the entire Adobe suite, AeroChat, Acrobat, and of course Office.

## Is there GPU passthrough?
Not at the moment, but we plan on eventually implementing GPU acceleration through paravirtualized drivers.

We have looked at MVisor Win VGPU Driver for OpenGL, which seems promising from our tests, but it's for a different hypervisor (not compatible with QEMU). Some other folks are also working on DirectX drivers but nothing that we can try out yet.

We have also looked into Looking Glass extensively, specifically their Indirect Display Driver which does not need a second GPU, because it'd be absolutely amazing to have it. We got the driver to compile and start via some hacks, but couldn't get much more than a black screen. The developer says it is not ready for general use yet at all, however we plan to integrate it once it is ready.

## Will I be able to configure my hardware using WinBoat?
For devices with USB, you can, but you need to do it manually for now. When eventually we add USB passthrough, you'll be able to do it from the WinBoat app itself.

Until then, you can modify the `docker-compose.yml` file in `~/.winboat` once you finished setting up WinBoat. You can add the appropriate USB devices [like this](https://github.com/dockur/windows?tab=readme-ov-file#how-do-i-pass-through-a-usb-device), followed by executing `docker-compose down` and `d`ocker-compose up -d` in the same folder.

## Does it run games with anti-cheat that don't run on Linux?
Unfortunately running games with kernel anti-cheat is not possible, as they block virtualization.

## Any possibility of adding Podman support as a Docker alternative?
Podman support is planned. We tried working on it, some contributors also tried working on it, but there's some issues with networking (specifically the guest server being unreachable) that prevent it from being functional for now.

## Will you make it into Flatpak?
This is on our to-do list, but it'll take some effort because Flatpak is pretty isolated from the rest of the system and apps, so we'd have to find a way to expose installed apps, the Docker binary, and the Docker socket, and many other utilities.

## So, am I able to run Office 365 on it?
Yes. : )