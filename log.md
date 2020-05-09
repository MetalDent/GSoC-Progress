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
- Side task:
    - Removed `-monochrome` from the icons conversion script and opened a PR
    
### Day 5 : May 8, Friday
- Side tasks:
    - Removing `-monochrome` is not the ideal solution as it's making all the entries of Logo headers as "0x00"
    - Tried various commands to perfect the conversion, finally BAndiT suggested some changes which worked well
    - To further perfect the icons, refer today's [logs](http://irc.apertus.org/index.php?day=08&month=05&year=2020) which have some links and ideas suggested by him
    - Maybe now we'll need to modify the DrawIcon() method as now the converted images are white with black background (or can invert the images)
    - Bertl suggested some more improvements which I'll try tommorrow and create a makefile instead of the script
- Established the remote connection to the server through ssh (note to self: don't forget the passphrase and fix the "A" key) 
- Played around the remote setup, Bertl said beta and remote will be added by this weekend
