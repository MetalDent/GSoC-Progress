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

### Day 6 : May 9, Saturday
- Did the image manipulation as suggested by Bertl:

`sed -i "/#c2bfbc/ s/fill-opacity:1/fill-opacity:0/" ApertusLogo.svg`

`convert ApertusLogo.svg -trim +repage ring.png`

- Resultant image -> https://pasteboard.co/J7AS6lqM.png

### Day 7 : May 10, Sunday
- Created the Makefile for the conversion script, took a little longer as I don't have much experience with that
- Had to tweak the process a bit
- Some changes/additions can be done:
    - writing `+negate -negate` doesn't seem right, so need to improve that part
    - add a feature in Makefile to automate the copying of data from xbm to header file
    
### Day 8 : May 11, Monday
- Modifed and made the makefile much shorter as it was simply repeating the whole process for all the icons
- Used `xbm:icon_name.h` in the conversion but that doesn't give a proper structure 
- So finally decided to use `sed` to convert xbm to header file, if BAndiT wont like that then will think of some other method

### Days 9-11 : May 12-14 Tuesday-Thursday
- Worked on the makefile
- Modified the structure of the sample.h

### Days 12-13 : May 15 & 16 Friday, Saturday
- Successfully connected with the remote-remote!
- Bertl helped with that as I didn't have experience with ssh
- Modified the ImageButton size and dimensions
- Also modified SetButton() in ButtonBar

### Days 14-15 : May 17, 18 Sunday, Monday
- Flashed firmware and bootloader in the remote setup
- Trying to use minicom but the setup doesn't have working USB I think, so we'll discuss today (Monday) about it
- minicom worked! (see notes.txt for relevant commands/info)

### Day 16 : May 19, Tuesday
- Started working for an ImageButton with image and text, see today's [logs](http://irc.apertus.org/index.php?day=19&month=05&year=2020)
- Tried making image on the left half and text on the right half but Sebastian suggested a better approach (I'm not entirely sure about that but trying to implement that)

### Day 17 : May 20, Wednesday
- Remote B is working now but minicom part is not yet configured, reminded Bertl about the remote camera access
- Have written some pointers about the remote setup in notes.txt, **please refer that if you forget anything**
- Worked on the ImageButton but something's wrong, trying to figure out

### Day 18 : May 21, Thursday
- Fnished with the image + text functionality of ImageButton, my calculations were correct but I was aligning the text in the center rather than to the left
- [Before](https://pasteboard.co/J97QZWU.png) and [After](https://pasteboard.co/J9nAO4t.png)
- Claimed [CheckBox task](https://lab.apertus.org/T1193)

### Day 19 : May 22, Friday
- Worked on PR[#15](https://github.com/apertus-open-source-cinema/AXIOM-Remote/pull/15), check it for details

### Day 20 : May 23, Saturday
- Solved some conflicts for PR[#17](https://github.com/apertus-open-source-cinema/AXIOM-Remote/pull/17/)
- Didn't work much as I'm getting my migraines back
