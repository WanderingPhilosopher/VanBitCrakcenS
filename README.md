# VanBitCrakcenS
VanBitCracken Spread

This is the VanBitCracken Spread Version. The Spread means that this specific version is geared towards covering ranges, not doing any random mode.  The random mode will come later.

This is a fork of Jean Luc Pons Vanity Search program and Telariust's Vanity Search Bitcrack program.  

You can use the flags/options that the program known as "Bitcrack" uses, except the -b -t -p options.  This program uses the grid size options that JLPs version used in version 15.  If you want to adjust grid size, use the -g option.  Since this is based off of version 15, the y grid size is hard coded so all you can adjust is the x grid size.

Example: -gpu -g 512 -gpuId 0 .

The other bonus feature of this program versus Bitcrack is it supports multiple GPUs.

The other difference from Bitcrack is this program will search for partial/strings of addresses and does not need a full address and can search for wildcards.

I will update this more in-depth later.

Other flags include:

-t for CPU threads (not optimized for CPU use, that was not the intent/focus)

-gpu for gpu use
-gpuId 0 (if more than one gpu use -gpuId 0,1,2,3,4  etc.)

-g to adjust x grid size; -g 256

--keyspace to enter your start and end range; example 80000:FFFFF

--continue to save work/progress; --continue continue.txt

-o for output/results file; -o outputfile.txt (if you do not add -o option, keys found will print on screen and to a text file named "KeysFound.txt")

-i for input file of addresses/strings; -i inputfile.txt

-r for rekey; -r 100000
the -r is important because in this spread version, it really tells the program how often to save your continue file in MKey/s. Based on your gpu and its MKey/s, you need to adjust the -r.  If your gpu's speed is 100 MKey/s and you want to save your continue file every minute, then you would calculate 60 (seconds) multiplied by 100 = 6000; so you would want to input -r 6000. If you do not input a -r it will go to the default of 10000 and depending on your card you could be saving every 5 to seconds (not recommended.)
You can also enter a single address/string at the end of your command line/batch file; comannd line ....... 19Hed12

Basic command line/batch file:
VanBitCrackenS1 -t 0 -gpu -gpuId 0 -r 150000 --keyspace 8000:FFFF -o output.txt -i input.txt (or just add address/string instead of input file)
pause

More to follow...
