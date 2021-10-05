# Wha?

I bought one of [these](https://www.ebay.com/itm/333986600758) Cavium CN8890 based blades.
Assuming it turns up and it isn't totally broken I will detail how to get it working here.

# Specs

- Mainboard dimensions ~50cm x 17cm. 
- [AST2400 BMC](http://www.aspeedtech.com/server_ast2400/)

# Work log

- 20210926
  BMC lights up when standby is supplied.
  I thought it might be +5V but there is a +5V LDO on the distribution board
  connected to that rail so that seemed weird. A similar 18 pin power connector
  on a similar Gigabyte server motherboard was +12V for standby. Based on the
  regulator and the other board I tried +12V on the standby rail and the BMC
  LED started blinking and nothing exploded.

- 20210926.1
  BMC JTAG 4 pin header is the uart for the BMC

- 20210929
  Unlocking the BMC
  The BMC password has been set and it's impossible to login.
  It should be possible to update the BMC firmware from u-boot and erase
  the settings at the same time but the updater command complains.
  I unlocked the BMC by pulling the flash chip out (SOP16 SPI NOR),
  erased it and flashed 773.bin to it.

- 20211005
  Memory,.. Non ECC DIMMs do not work. Current registered ECC DIMMs
  I have don't complete the memory setup most of the time. Usually the
  second channel on the second CPU. Moving them around changes nothing
  so it's possible the board is broken or it just doesn't like these
  DIMMs. DIMMs listed as working in gigabytes list on order.

# Links

https://www.servethehome.com/gigabyte-r120-t30-overview-first-cavium-thunderx-system/
