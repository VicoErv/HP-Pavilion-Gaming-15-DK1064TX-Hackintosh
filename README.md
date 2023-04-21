# HP Pavilion Gaming 15 DK1064TX
After 2 years of trial and error.

Specs:
- Intel Core i5-10300H
- Intel UHD 630 Graphics
- 16 GB 2933hz
- Midas Force 1TB SSD NVME M.2 Gen 3 x4 2280 Form Factor
- RAMOS 2.5 inch SATA 1TB SSD Media
- Intel® Wi-Fi 6 AX 201 (2x2) and Bluetooth® 5 Combo (Supporting Gigabit file transfer speeds)
- Integrated 10/100/1000 GbE LAN
- Audio by B&O; Dual speakers; HP Audio Boost 1.0 (ALC285)


What's working:
- QE/CI
- Audio
- USB Ports + USB C
- Battery Indicator 
- Change brightness using keyboard
- Change audio using keyboard

Not working:
- Sleep
- Trackpad (ELAN0710, interrupt 0x4a, Pin 0x32)
- USB-C to DP Display output
- HDMI Display output (Workaround using Display-Link, but it's very not recommended, i bought the adapter and the quality is not bearable)

Footnote:
Why it's take so long up until 2 years to get this working? Well, the DSDT table make it not bootable, because the `HS14` is wrapped inside `PCHS == PCHH` checks. And I don't know what are those, so I just move the `Device (HS14)` outside the that conditional scope. And this is not documented anywhere, or it's just me that bad at searching for something. But, now I'm glad it's working, I can continue to work using Xcode again.
