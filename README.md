a4tech-bloody-linux-driver
====================

Linux utility for config a4tech bloody mouse series.
This tool allows setting backlight level, enable/disable wheel of A4TECH wired mouse (USB connected), e.g. A4TECH V7M.

# Build instructions
## Fedora 29
```
dnf install gcc-c++ cmake libusbx-devel
```
## Ubuntu / Debian
```
sudo apt install libusb-1.0-0-dev cmake g++
```
```
git clone --recursive https://github.com/Mr-Precise/a4tech-bloody-linux-driver
cd a4tech-bloody-linux-driver
mkdir build && cp mice.ini build/ && cd build
cmake -G "Unix Makefiles" ..
make
```

# Usage
```
sudo ./bloody
Possible parameters:
  -h        this help message
  -r        reset mouse
  -l        list devices
  -d num    specify device address
  -b        get backlight level
  -B lvl    set baclklight level [0-3]
  -W        disable mouse wheel
  -w        enable mouse wheel
  -S slot   set sensitivity for a slot, followed by -x and -y params
    -x num    x sensitivity
    -y num    y sensitivity

sudo ./bloody -l
Device Bloody V7M (address 2)

sudo ./bloody -d 2 -b
Current backlight level: 1
```
