# Course Challenge Scenario 

The SOC has received an anonymous report that a user is potentially exfiltrating data from the company. An image of the user’s hard drive has been taken, and you are responsible for analyzing the contents of a perfect copy to find any evidence of malicious activity. Using your newly developed skills, search through the folders and files using techniques to uncover 4 pieces of hidden information (each piece of evidence will contain the string {1 of 4} or similar). You will be tested on your ability to discover this information using all of the techniques taught in this course; Linux CLI navigation, identifying incorrect file extensions, identifying hidden files/folders, steganography, and password cracking.

# Tools needed 
- Vm software virtualbox or  vmware
- kali linux cvm
- Challenge Disk Image (.zip file for ease-of-use. Download this to your Kali VM, unzip, and get going! Bottom of page)

# Commands

- ls -a (Allows us to identify files hidden using filenames beginning with “.” in the current directory)
- cat/heads/strings (Allows us to potentially find hidden text strings in image and audio files, or read text files from the CLI)
- fcrackzip (Allows us to crack password protected .zip files)
- steghide (Allows us to retrieve files hidden in image and audio files)
- file (Allows us to see what the true file-type of the file is, even if the extension has been changed to trick us)
# Evidence 1 


1. We launch the kali linux vm and download the file.
2. Unzip the file using the command and use the name J Harrison Disk Image 10.09.2019.
3. We navigate to the directory path in downloads using the command cd 'J Harrison Disk Image 10.09.2019'
4. Using the tree command to display the directory structure in a tree-like format. It shows the hierarchy of directories and their subdirectories along with files. If you dont have the command use sudo apt-get install tree
<img width="1077" height="260" alt="j harison disk" src="https://github.com/user-attachments/assets/d8863127-8fe1-4c0a-bac7-dc856f15a958" />


<img width="1226" height="1056" alt="tree1" src="https://github.com/user-attachments/assets/bc65fbd5-1624-42c1-99cf-1b2840ff37d1" />

<img width="1126" height="865" alt="tree2" src="https://github.com/user-attachments/assets/95d4e46a-b7ed-4197-93eb-620c700b0c4a" />

After some time in the drive we find a directory called "to-do". With the command ls -a, we find a hidden zip file. We see that the file has been encrypted with a password.

<img width="1810" height="942" alt="file zip" src="https://github.com/user-attachments/assets/9855cfcc-c02d-4aaa-9f14-1df75fee3aae" />

<img width="1630" height="393" alt="password fail" src="https://github.com/user-attachments/assets/b99fa4c3-0e4a-4415-b5f4-5d9079696132" />

We did not find any passwords in the Harrison disk drive so we gonna use a dictionary attack with fcrackzip to find the password of the zip file.
We find the password **vendy13031988*.

<img width="1607" height="270" alt="dictionary attack" src="https://github.com/user-attachments/assets/c3d84a85-2ccc-4c30-8213-a5bba0d7999e" />

Now that we got the password we go ahead and unzip the file and we find a txt and use cat the find what's inside it.

<img width="1636" height="682" alt="file unzip" src="https://github.com/user-attachments/assets/e2847833-f64b-483e-8801-783649456fe5" />


# Evidence 2 
We examine the images directory. the laptop.jpg and office 2.jpg files had an unusually large byte size for a typical image, making them sus. 



<img width="1768" height="1084" alt="evid 2" src="https://github.com/user-attachments/assets/09284c5f-2e90-4863-bf06-7b9f07c628c0" />

use steghide commands on both the files. Both files are stegofiles. we need to find the passwords.

<img width="1353" height="564" alt="stegofiles" src="https://github.com/user-attachments/assets/c4959a1e-0151-4725-977c-1b12a2aac5c3" />

in the saved emails dir we find in form1.jpg useful info. Simon, I have usernames and passwords for the VPN. Still on my work PC. Don't want to risk emailing them just yet. When I do, the file is a .jpg image + password for extraction is password. Use steghide. Talk again soon. This message shows that the .jpg stegfiles all have a password of password.

<img width="1370" height="813" alt="saved emails cd" src="https://github.com/user-attachments/assets/d1fbbf08-fc3a-4a68-a338-3a9e66ef5ed6" />


<img width="1898" height="628" alt="pass is password" src="https://github.com/user-attachments/assets/116bcda1-fb75-4b95-bbe5-3f70816db73a" />

























































# General Knowledge Questions 


- Question 1: When considering the order of volatility, which is the MOST volatile form of evidence? Cache
- Question 2: What is the Chain of Custody in regard to digital forensics? Paper trail for evidence that shows where it has been, and who has been in possession of it.
- Question 3: An employee is under investigation, and you are sent to look at his laptop. You discover that it is locked, but you have the user’s password to unlock it. What should you do next? Wait for the user and get them to sign-in
- Question 4: Can social-media posts be counted as a form of electronic evidence? yes 
- Question 5: Which one of the following evidence types holds the most value in court? Real Evidence
- Question 6: When cracking ZIP passwords using fcrackzip, what is the flag used to conduct a brute force attack, with lowercase letters and numbers? format: -(flag) -(flag) (values) -b -c a1
- Question 7: Digital Forensics entails… The identification, preservation, and analysis of evidence found on electronic devices.
- Question 8: What does HTCIA stand for in regard to Digital Forensics? High Technology Crime Investigation Association
- Question 9: Computer Forensics and Data Recovery are the same thing, true or false? false
- Question 10: Corporate Policies can dictate which of the following? all of the above



# Practical Challenge Questions

- Question 1: [Evidence 1/4] What is the name of the file where the evidence was found? (filename and extension) 

employeedump.txt

- Question 2: [Evidence 1/4] What is the name of the directory your in where this evidence was found?

to-do

- Question 3: [Evidence 1/4] What piece of evidence have you found? 

Employee information

- Question 4: [Evidence 2/4] What is the name of the file where the evidence was found? (filename and extension)

laptop.jpg

- Question 5: [Evidence 2/4] What is the name of the directory your in where this evidence was found?
Images

- Question 6: [Evidence 2/4] What piece of evidence have you found? 

List of employee passwords

- Question 7: [Evidence 3/4] What is the name of the file where the evidence was found? (filename and extension)

 posidon.xml

- Question 8: [Evidence 3/4] What is the name of the directory your in where this evidence was found?

 week 10

- Question 9: [Evidence 3/4] What piece of evidence have you found?

 Office Locations

- Question 10: [Evidence 4/4] What is the name of the file where the evidence was found? (filename and extension)

  bootstrap.min.abc

- Question 11: [Evidence 4/4] What is the name of the directory your in where this evidence was found?

  css

- Question 12: [Evidence 4/4] What piece of evidence have you found? 
  
  Colin’s information

  















