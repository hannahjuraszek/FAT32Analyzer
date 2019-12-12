AUTHORS:

	Hannah Juraszek
	Jordan Gillespie


VERSION: 

	12 December 2019


DESCRIPTION:

	A digital forensics tool that parses through an image of a FAT32 file system and can
	perform the following tasks: 
		1) restore a missing or modified boot sector using the backup
		2) parse through the BPB (Bios Parameter Block) for information about the file system
		3) locate and repair illegal characters in the root directory
		4) report if the attribute type of a directory entry is invalid
		5) repair reserved bytes that have been overwritten


INSTRUCTIONS:

	To start the FAT32Analyzer on a Windows computer, double click the FAT32Analyzer.bat file. 
	This will bring up the command line asking for the path of the FAT32 image to parse. If the 
	image is not in the same directory as the .bat file, an absolute path is needed. Next, input 
	the desired output file name with a .dd extension. Again, use an absolute path if needed.
	After inputting the file names, if the file names are correct, press enter and the tool will 
	begin. The repaired image will be outputted to the desired output file name.
	
	To start the FAT32Analyzer on a Linux/MacOS computer, open terminal and navigate into the 
	directory that houses FAT32Analyzer.java. In the terminal, type the command 'javac 
	FAT32Analyzer.java' to compile the program. Then type the command 'java FAT32Analyzer
	theNameOrPathOfYourInputFile.dd theNameOrPathOfYourDesiredOutputFile.dd' and press enter.
	The tool will begin, and the repaired image will be outputted to the desired output file
	name.
	
	Any discrepancies that could not be automatically repaired will be reported to the user via 
	the terminal, including the offset at which they occur.
	


FILES INCLUDED:

	FAT32Analyzer.java
	FAT32Analyzer.bat
