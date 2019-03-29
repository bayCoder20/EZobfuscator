# EZobfuscator_v0.1.0_beta

------------
I. Introduction
------------
This program is for obfuscating variables in VBA (VB) code making source code more difficult to read and reverse engineer.  
All comments and empty lines are also removed.  (more languages to be supported)

Download Program Here: https://github.com/bayCoder20/EZobfuscator/releases

------------
II. PC Requirements
------------
- OS: Windows (developed/tested on Windows 10 with MS Excel)
- Java: Java 8 or newer  (developed/tested on Java 8)
	
------------
III. Quick Start Directions
------------
1. After unzipping file, set the path for code to be obfuscated in "obfuscatorConfig.properties". (ex. c:\workspace\vanillaCode.vbs)
2. Double click the "obfuscator_vX.XX_beta.jar" file to start the program.
3. The obfuscated code will be in the root directory of this program.

------------
IV. File List
------------
obfuscatorConfig.properties	- Contains the setup configuration for each back test execution
obfuscator_vX.XX_beta.jar	- Program executable file, double click to initiate back test after configuration is complete
README.txt			- This file describing program contents and operations

-------------
V. Folder List
-------------
logs				- REQUIRED - Location of log files, one will be created for each run.

-------------
VI. Program Inputs
-------------
The program takes two files file for input, a configuration properties file and a text file with the list of variables to be obfuscated. 
The program home directory is where the location of the obfuscator_vX.XX_beta.jar file is saved.

Properties File - This file contains the configuration options.

Variable List - This file is used to acquire the list of variable names that will be obfuscated.  Currently, the format of each variable name can be
read in the file as carriage-return separated values or comma separated values or a combination of both. Any text below this blank line will not effect the operation of the program
and can be used to store alternate lists and notes. See provided sample files.

-------------
VII. Program Outputs
-------------
The program will output one log file in the "logs" folder.  Each log file will contain a record of the original code, a map list of the variable names matching the obfuscated names, and the obfuscated code.
Each record inclusion can be toggled true/false as necessary in the configuration options.  

-------------
VIII. Features
-------------
- Obfucsation of VBA(VB) variable names.
- Customize list of characters to be used for obfuscation.
- Customize number of characters (NOTE: Max allowed length of a VBA variable name is 255 characaters).
- Options to randomize number of characters in variable names between two ranges.
- Option to automatically acquire list of variables from original code using "Dim" as a locator.
- Removes all comments.
- Removes all blank lines.

-------------
IX. Upcoming Features
-------------
- The ability to support additional script style languages.
- Obfuscation of multiple files.

-------------
X. Program Setup
-------------
After Downloading "obfuscator_vX.XX_beta.jar"
1. Unzip file to location of your choice.

Complete "obfuscatorConfig.properties" Settings
1. Set File Path For Code To Be Obfuscated (c:\workspace\vanillaCode.vbs)
2. Set Output File Path And File Name Of Obfuscated Code (Default is program directory)
3. Set Option To Automatically Acquire Variable Names. (Default is TRUE)
4. Set File Path Of Variable List (as needed)
5. Set list of characters used in obfuscation. Invalid characters will be automatically removed from list. 
   (Default characters are "abcdefghijklmnopqrstuvwxyz0123456789")
6. Set Minimum Number of Characters In Variable Name (Default is 35)
7. Set Maximum Number of Characters In Variable Name (Default is 35)
8. Set Option To Output Original Code In Log File. (Default is TRUE)
9. Set Option To Output Map Of Obfuscated Variable Names In Log File. (Default is TRUE)
10. Set Option To Output Original Code In Log File. (Default is TRUE)

-------------
XI. Program Operation
-------------
1. Once setup is complete, double click the "obfuscator_vX.XX_beta.jar" file to start the program.
2. Review the new "_Log.txt" file in the "logs" folder for details and any errors.
