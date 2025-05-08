# PS4Linux-ArchDrivers
### Drivers for running arch based distro
___
These aren't exhaustive lists, just the stuff I tested.

Tested with [DFAUS-git's 5.4.99 Baikal Kernel](https://github.com/DFAUS-git/ps4-linux-kernel-5.4.99-baikal) (Upstreamed to 5.4.291) on a CUH-2215B PS4
### Working
* XFCE4
* OpenGL (glxgears, SuperTuxKart, Terraria native, Terraria through Wine w/ WineD3D OpenGL)
* YouTube @ 4K on Firefox
### Broken
* Vulkan (vkcube causes the entire screen to freeze and artifact, can be recovered by either rebooting or closing the program)

**Note: I'm not sure if this is an issue with mesa or if it's a kernel issue**

------------

## How do I install the drivers?
If you want to install the drivers using the precompiled files, run ```sudo pacman -U *``` in the 'Compiled/latest' folder.

## How do I compile the drivers?
If you want to compile the drivers, run ```makepkg -sr``` in each folder inside 'SRC'.

### Note for mesa:
You only need the **mesa**/**lib32-mesa** package, the other packages are extranious

`makepkg` and it's flags are better explained [here](https://archlinux.org/pacman/makepkg.8.html)
## I have an issue/error

If it isn't already listed as [Broken](#broken), you can make an issue.

### Current Package Versions:
lib32-libdrm: 2.4.124-1<br>
libdrm: 2.4.124-1<br>
lib32-mesa: 1:25.1.0-1<br>
mesa: 1:25.1.0-1<br>
xf86-video-amdgpu: 23.0.0-2<br>

-----------

#### Credit
- [@failoverflow](https://github.com/fail0verflow)
- [@Ps3itaTeam](https://github.com/Ps3itaTeam)
- [@codedwrench](https://github.com/codedwrench)
- [@rinsuki](https://github.com/rinsuki)
- [@Hakkuraifu](https://github.com/Hakkuraifu)
