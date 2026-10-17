# Intro to linux cli

This lessons is designed for students that don’t have any experience using the linux command-line interface, or a terminal, to complete basic tasks. 

# Activity and Quiz

1. Lauch kali vm machine and download the file.
2. Unzip the file and name it SBT_Linux_CLI-2.
3. Navigate to that directory.
4. Use ls -a to list all files and dir and the hidden ones.

<img width="960" height="382" alt="sbt linux cli2" src="https://github.com/user-attachments/assets/cbc8255a-f547-4932-a3de-9e68bed36476" />

Q1. What is the phrase on line 8 of the first text file you come across?
The first file we come across is asdafada.txt. we run the cat command and in line 8 we see the phrase is **there's a snake in my boot**.
<img width="852" height="445" alt="line 8" src="https://github.com/user-attachments/assets/62d4d1e5-735b-4ac4-a5fa-7a6cef67380f" />


Q2. How many images are in the /Home/PersonalFiles/Photos/ directory?

From the SBT_Linux_CLI-2 directory we navigate to cd Home/PersonalFiles/Photos and the use ls -a to list everything. We get 3 image files.

<img width="1170" height="277" alt="3 images" src="https://github.com/user-attachments/assets/c0387fd0-f3d8-483a-a3ac-809f16780225" />

Q3. There are two files with incorrect extensions, what are their filenames? (Without the file extensions)

the two files are doggo and pancakerecipe

<img width="1171" height="520" alt="incoreect files extension" src="https://github.com/user-attachments/assets/d8c35366-b9d8-4131-871f-8c9351af9e10" />

Q4. One of these incorrect extension files hides a message, what is it?

WE use the mv command to rename the files to jpeg and png.

the file pancakerecipe.png has the secret message: SIERRA ECHO CHARLIE ROMEO ECHO TANGO



<img width="1752" height="777" alt="secfret message" src="https://github.com/user-attachments/assets/2e81401f-98a1-4afc-9f50-d411948b5f94" />


Q5. There is a text file with the string “bankdetails” as part of the filename. What is the full filename?

The file is named: 11_09_2019_statement_bankdetails.txt

<img width="1390" height="477" alt="text file name" src="https://github.com/user-attachments/assets/c6ca2d25-8062-4dcb-af38-a040a8965261" />


Q6. What is the flag value inside the text file within the hidden directory?
-106019BAL0S0A1 

We run ls -a to find hidden files we navigate to .private folder and we find readme.txt we cat and get the flag value inside the file.

<img width="1387" height="627" alt="flag value" src="https://github.com/user-attachments/assets/880b5831-69b9-4fd3-8521-130b23533ae4" />

Q7. How many images are in the /Home/ directory? (Including files that SHOULD be images, if any)?

we go back to that dir use ls -a to show all files and we see that there are 5 images.

<img width="1298" height="315" alt="5 images in home dir" src="https://github.com/user-attachments/assets/2bff81b7-faa8-4aae-ba99-ecc1c26aeed7" />























