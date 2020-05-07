# Google Summer of Code'20 @apertus Assocation

## Community Bonding Period:

### Day 1 : May 4, Monday
Got the selection results, did not work much.

### Day 2 : May 5, Tuesday
- Looked at Bootloader code
- Installed radare2/Cutter and XC32, the latter one did not work so will install that tomorrow

### Day 3 : May 6, Wednesday
- Successfully installed XC32 and built Bootloader and Firmware
- Played around the Cutter and compared the .elf files of Bootloader and Firmware
- Read the blog posts suggested by BAndiT
 
### Day 4 : May 7, Thursday
- Following pointers about Cutter (learnt from BAndiT) :
    - use "aaaa" mode as it gives better analysis
	- the top search bar is used for searching addresses, strings etc
	- "hexdump" is useful to see what data is stored in which address
- Common/procdefs.ld has information about the addresses for various sections
- Verified the data (like apertus_text) and addresses from the .elf file, procdefs and the actual data
