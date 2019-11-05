# pidp11 ↔ cyc1000 adapter

This is an adapter board to connect the
[CYC1000](https://shop.trenz-electronic.de/en/Products/Trenz-Electronic/CYC1000-Intel-Cyclone-10/)
FPGA module to the
[PiDP-11, PDP-11/70 front panel replica](https://obsolescence.wixsite.com/obsolescence/pidp-11).

It is intended to be used with [PDP2011](http://pdp2011.sytse.net/), an FPGA
implementation of the PDP-11 by Sytse van Slooten.

In addition to routing the necessary pins to the panel, the board also
includes some components for use with the PDP2011:

* Micro-SDCard connector
* USB-UART bridge using the [CP2102](https://www.silabs.com/products/interface/usb-bridges/classic-usb-bridges/device.cp2102)
* Pin headers for connecting to [PMODNIC100](https://store.digilentinc.com/pmod-nic100-network-interface-controller/)

## Design considerations

* Power input from PiDP-11 header via VIN
* CYC1000 is placed underneath the adapter for clearance with the back panel
* CP2102 is bus-powered, and will not power the rest of the circuit
* The packages are chosen based on what I happen to have in my shelves

## TODO

* Actually test if the design works
* Replace CP2102 footprint with something easier to solder
* Integrate ENC424J600 to the board
