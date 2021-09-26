# Wha?

I bought one of [these](https://www.ebay.com/itm/333986600758) Cavium CN8890 based blades.
Assuming it turns up and it isn't totally broken I will detail how to get it working here.

# Specs

- Mainboard dimensions ~50cm x 17cm. 
- [AST2400 BMC](http://www.aspeedtech.com/server_ast2400/)

# Work log

- 20210936 BMC lights up when standby is supplied. 
  I thought it might be +5V but there is a +5V LDO on the distribution board
  connected to that rail so that seemed weird. A similar 18 pin power connector
  on a similar Gigabyte server motherboard was +12V for standby. Based on the
  regulator and the other board I tried +12V on the standby rail and the BMC
  LED started blinking and nothing exploded.

# Links

https://www.servethehome.com/gigabyte-r120-t30-overview-first-cavium-thunderx-system/
