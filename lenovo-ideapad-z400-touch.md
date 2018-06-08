Linux ideapad 3.12.9-1-ARCH #1 SMP PREEMPT Sun Jan 26 09:01:37 CET 2014 x86_64 GNU/Linux

lspci | grep VGA
00:02.0 VGA compatible controller: Intel Corporation 3rd Gen Core processor Graphics Controller (rev 09)
01:00.0 VGA compatible controller: NVIDIA Corporation GF108M [GeForce GT 635M] (rev a1)

local/libva 1.2.1-1
local/libva-intel-driver 1.2.2-2
local/libva-vdpau-driver 0.7.4-1

local/libvdpau 0.7-1
local/libvdpau-va-gl 0.3.2-1

local/xf86-video-intel 2.99.907-2 (xorg-drivers xorg)


[ecc@ideapad vdpauinfo]$ vainfo 
libva info: VA-API version 0.34.0
libva info: va_getDriverName() returns 0
libva info: User requested driver 'vdpau'
libva info: Trying to open /usr/lib/dri/vdpau_drv_video.so
libva info: Found init function __vaDriverInit_0_33
[VS] Software VDPAU backend library initialized
libva info: VA-API version 0.34.0
libva info: va_getDriverName() returns 0
libva info: User requested driver 'vdpau'
libva info: Trying to open /usr/lib/dri/vdpau_drv_video.so
libva info: Found init function __vaDriverInit_0_33
^C
[ecc@ideapad vdpauinfo]$ vdpauinfo 
display: :0 screen: 0
[VS] Software VDPAU backend library initialized
libva info: VA-API version 0.34.0
libva info: va_getDriverName() returns 0
libva info: User requested driver 'vdpau'
libva info: Trying to open /usr/lib/dri/vdpau_drv_video.so
libva info: Found init function __vaDriverInit_0_33
^C

XFS tips

Increase AG (allocation groups) count:

mkfs.xfs –f –d agcount=32

https://ask.fedoraproject.org/en/question/41664/optimization-for-an-ssd/

https://superuser.com/questions/228657/which-linux-filesystem-works-best-with-ssd



fdisk will also create partitions at the 1024KB border if started with the "-cu" flags.
