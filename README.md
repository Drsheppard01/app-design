# Some ideas from a non-developer for developers on what technologies improve the user experience on Linux

1. Self-extractable compressed tar archive with Installer like as [mojosetup](https://github.com/icculus/mojosetup). Software that implements this concept: [NVIDIA drivers](https://www.nvidia.com/Download/driverResults.aspx/193095/en-us/), [DaVinci Resolve](https://www.blackmagicdesign.com/products/davinciresolve)
2. Single binary-file for Linux on container like as AppImage, but with full integrate, and works glibc-free distros
3. Using declarative files for installation. Example: [rinstall](https://github.com/danyspin97/rinstall), [One Click Install](https://en.opensuse.org/openSUSE:One_Click_Install) by openSUSE, [pkger](https://github.com/vv9k/pkger)

# Disadvantages of popular distro-independent formats

## AppImage
 
 1. Doesn't work on non-glibc distro such as Alpine, Void, Kiss (but it looks like this will be fixed soon)
 2. Host system libraries and container libraries are mixed
 3. No mandatory integration
 4. No mandatory isolation (this problem is partially solved by aisap, firejail)
 
 ## Flatpak
 
 1. Using a large number of directories e.g. /var/app/ $HOME/.var/app
 2. Files remain after deletion, which are deleted by a separate command or manually
 3. No graphical installer for flatpakref (elementatyOS offers sideload - and it's a great solution to this problem)
 
 ## Snap
 
 1. Mount image when system is started (it is this circumstance that puts a strain on the system and also discourages users) instead mount by click, when user want to use this app
 2. There is no automatic mechanism to remove old versions (e.g. after a certain number of successful runs by the user)
 3. Aggressive policy of imposition in the style of #UpgradingToWindows10
