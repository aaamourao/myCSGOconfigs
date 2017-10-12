# My *Counter-Strike: Global Offensive* config files

Repo for sharing my **CSGO** config files, hardware setup and tips. I'm
running it at **GNU/Linux Ubuntu 16.04 LTS** as it is officialy supported by
**Steam** (For life, I'm a **Fedora GNU/Linux** user and contributtor). The
game is **OpenGL** based, _**Source Engine**_, so my system is under __admgpu__ *Open Source*
driver stack, instead of __amdgpu-pro__, which is better for __*Source2 Engine*__,
**Vulkan**, and so on... _e.g. **Dota 2**_

## File list

* config.cfg: Roughly based on [**SK | Coldzera**](https://go.twitch.tv/coldzin) config file
* treinamento.cfg: Small config file for practicing alone or against bots
* autoexec.cfg: A shameful copy of [**SK |
  Coldzera**](https://go.twitch.tv/coldzin) autoexec config file

## Video settings

Based on [**SK | Fallen**](https://go.twitch.tv/gafallen) video settings:

![CSGO -> Options -> Video
Settings](/images/videosettings.jpg)

## Mouse: Xinput properties

On `~/.bashrc`:

```bash
# Mouse Settings
xinput --set-prop 11 "Device Accel Constant Deceleration" 1.35
xinput --set-prop 11 "Device Accel Velocity Scaling" 1
xinput set-prop 11 'Device Accel Profile' -1
```
List of all properties:

```bash
[madc0w@heima]: myCSGOconfigs $ xinput list-props 11
Device 'HID-compliant Mouse HID-compliant Mouse':
        Device Enabled (137):   1
        Coordinate Transformation Matrix (139): 1.000000, 0.000000, 0.000000,
0.000000, 1.000000, 0.000000, 0.000000, 0.000000, 1.000000
        Device Accel Profile (285):     -1
        Device Accel Constant Deceleration (286):       1.350000
        Device Accel Adaptive Deceleration (287):       1.000000
        Device Accel Velocity Scaling (288):    1.000000
        Device Product ID (257):        7511, 5
        Device Node (258):      "/dev/input/event4"
        Evdev Axis Inversion (289):     0, 0
        Evdev Axes Swap (291):  0
        Axis Labels (292):      "Rel X" (147), "Rel Y" (148), "Rel Vert Wheel"
(297)
        Button Labels (293):    "Button Left" (140), "Button Middle" (141),
"Button Right" (142), "Button Wheel Up" (143), "Button Wheel Down" (144),
"Button Horiz Wheel Left" (145), "Button Horiz Wheel Right" (146), "Button Side"
(295), "Button Extra" (296), "Button Unknown" (260), "Button Unknown" (260),
"Button Unknown" (260), "Button Unknown" (260)
        Evdev Scrolling Distance (294): 1, 1, 1
        Evdev Middle Button Emulation (271):    0
        Evdev Middle Button Timeout (272):      50
        Evdev Middle Button Button (273):       2
        Evdev Third Button Emulation (274):     0
        Evdev Third Button Emulation Timeout (275):     1000
        Evdev Third Button Emulation Button (276):      3
        Evdev Third Button Emulation Threshold (277):   20
        Evdev Wheel Emulation (278):    0
        Evdev Wheel Emulation Axes (279):       0, 0, 4, 5
        Evdev Wheel Emulation Inertia (280):    10
        Evdev Wheel Emulation Timeout (281):    200
        Evdev Wheel Emulation Button (282):     4
        Evdev Drag Lock Buttons (283):  0
```

## Hardware and Software setup

External hardware:

* Fortrek **Spider Venom** mouse
* Fortrek **Venom 2** keyboard

Main hardware:

```bash
[madc0w@heima]: WorkSpace $ inxi -F
System:    Host: heima Kernel: 4.10.0-37-generic x86_64 (64 bit) Desktop: Gnome
3.18.5
           Distro: Ubuntu 16.04 xenial
Machine:   System: ASUS product: All Series
           Mobo: ASUSTeK model: SABERTOOTH Z97 MARK 2 v: Rev 1.xx
           Bios: American Megatrends v: 1202 date: 06/17/2014
CPU:       Quad core Intel Core i5-4690K (-MCP-) cache: 6144 KB
           clock speeds: max: 4500 MHz 1: 3810 MHz 2: 3536 MHz 3: 3501 MHz 4:
3488 MHz
Graphics:  Card: Advanced Micro Devices [AMD/ATI] Device 67df
           Display Server: X.Org 1.19.3 driver: amdgpu Resolution:
1920x1080@60.00hz
           GLX Renderer: Gallium 0.4 on AMD POLARIS10 (DRM 3.9.0 /
4.10.0-37-generic, LLVM 4.0.0)
           GLX Version: 3.0 Mesa 17.0.7
Audio:     Card-1 Intel 9 Series Family HD Audio Controller driver:
snd_hda_intel
           Card-2 Advanced Micro Devices [AMD/ATI] Device aaf0 driver:
snd_hda_intel
           Card-3 Logitech G930 driver: USB Audio
           Sound: Advanced Linux Sound Architecture v: k4.10.0-37-generic
Network:   Card: Intel Ethernet Connection (2) I218-V driver: e1000e
           IF: eno1 state: up speed: 100 Mbps duplex: full mac:
10:c3:7b:6d:07:c6
Drives:    HDD Total Size: 240.1GB (42.6% used) ID-1: /dev/sda model:
SSD2SC240G1CS176 size: 240.1GB
Partition: ID-1: / size: 204G used: 80G (42%) fs: ext4 dev: /dev/dm-0
           ID-2: /boot size: 473M used: 187M (42%) fs: ext2 dev: /dev/sda2
           ID-3: swap-1 size: 17.12GB used: 0.00GB (0%) fs: swap dev: /dev/dm-2
RAID:      No RAID devices: /proc/mdstat, md_mod kernel module present
Sensors:   System Temperatures: cpu: 29.8C mobo: 27.8C gpu: 45.0
           Fan Speeds (in rpm): cpu: 0
Info:      Processes: 260 Uptime: 46 min Memory: 5655.1/15986.3MB Client: Shell
(bash) inxi: 2.2.35
```
