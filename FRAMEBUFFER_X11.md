# Genesys 2: simple-framebuffer + X11

Requires a bitstream with the DVI framebuffer core: 320x240 RGB565 buffer at 0x83000000, doubled to 640x480.

Build:   make            (output: install64_genesys2/sdcard.img)
Test:    dd if=/dev/zero bs=640 count=240 | tr '\000' '\377' > /dev/fb0
X:       started at boot by S40xorg; xorg.conf preloads fbdevhw and shadow modules.

