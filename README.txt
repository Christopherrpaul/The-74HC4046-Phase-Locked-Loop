This repository of code is an accessory to the EDN article 'Designing Phase-Locked Loops (PLLs) with the 74HC4046" whose publication date is TBD, and whose editor might change the article title.

Signetics/Philips released "Phase-locked Loop Circuits: 74HC/HCT4046A and 74HC/HCT47046A HCMOS designer's guide - advance information" with contains a wealth of information about how to use the referenced parts and indeed, pretty much any Phase-locked loop (PLL). The .pdf file is a searchable version of that document. The guide mentions the existence of an MSDOS program which performs much of the necessary computations. The code is found in the .zip file.

You'll need software to run the code on most contemporary computers. I recommend using DOSBOX.   https://www.dosbox.com/download.php?main=1 is one site with a program that allows MSDOS programs to run. For Windows, I recommend creating a directory C:\DOSDIR into which MSDOS executable code can be extracted. Download, install and run DOSBOX and type:

	MOUNT c c:\dosdir
	C:
	DIR

You should then be able to run PLL_BODY.EXE as if you were on DOS-compatible machine. 
 
Although the 74HC4046 is characterized for operation from 3 to 6V, the program for some reason provides the VCO component values C1, R1 and C2 for 5V operation only. However, the .xlsm Excel spreadsheet accepts as input a number of parameters that the MSDOS program will produce when it is run with any 3 - 6V value. The spreadsheet output includes the three VCO component values and also allows you to select a more convenient value of C1 for which it determines the associated values of R1 and R2. It also checks if the three component values are within the manufacturer-specified ranges. The program is intended for use with Nexperia ICs, but I have used it successfully with the Texas Instruments part. You might want to tweak some of the resistor values in the latter case, though.