# Using a LG Ultrafine 5K Display with Windows 10

I recently built a PC for playing games. I have a nice monitor I wanted to make use of and don't have enough desk space to warrant a third monitor. After a lot of research, I've managed to get my Thunderbolt 5K display working in Windows 10 at full 5K resolution at 60Hz. This requires a GPU with 2 Display Ports.

In order to do this, you need a motherboard that supports Thunderbolt 3. My PC is built on an Asus TUF Gaming B550-Plus motherboard with an AMD Ryzen 5800x. 

You will also need to buy an appropriate Thunderbolt PCI-Express card. In my case, this was an Asus ThunderboltEx 3-TR. TR is an abbreviation of `Titan Ridge`, the chipset codename. The card is a half size PCI-e slot that requires a 6-pin power connector from the PSU. The card then connects to a 14-pin header on the motherboard and via another USB motherboard header. From my research, there are variants of these expansion cards, depending on the supported chipset. Make sure you get one that is compatible with your motherboard. Be sure to cross reference motherboard pin-outs from your manual to ensure the connectors match.

Once the card is seated and connected to the motherboard, it needs to be enabled in BIOS. On my Asus B550 motherboard, the options were hidden under `Advanced (F7) > Advanced > AMD PBS`

### BIOS Settings

* Data Link Feature Exchange - *Enabled*
* Thunderbolt Support - *Enabled*
* Thunderbolt Host Chipset - *Enabled*
* TR HR FPB Capability - *Enabled*
* Thunderbolt Security Level - *User Authorization*
* Thunderbolt Boot from TB - *Disabled*
* Thunderbolt MMIO Resource - *Full Size*
* Thunderbolt Wake Up Command - *GO2SX Command*

### Windows 10 Configuration

* Install `Intel Thunderbolt Driver` from your expansion card manufacturer and reboot.
* Connect the Display Port cables to your GPU, connect the other end to you expansion card.
* Connect your LG Ultrafine Display to the Thunderbolt card. (Port 1 is recommended)
* Set your resolution to 5120 x 2880. Check your GPU options, I was able to enable 10bit color, which is supported by this monitor

### Adjusting Brightness

* The LG Ultrafine monitors have no onscreen display or buttons to adjust brightness, so you need to use [this application from the Windows Store](https://www.microsoft.com/en-us/p/lg-ultrafine-brightness/9n5mj2fq4gww?activetab=pivot:overviewtab). (Older open source solutions didn't work for me.)
