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


1. We launch the kali linux vm and download the file.
2. Unzip the file using the command and use the name J Harrison Disk Image 10.09.2019.
3. We navigate to the directory path in downloads using the command cd 'J Harrison Disk Image 10.09.2019'
4. Using the tree command to display the directory structure in a tree-like format. It shows the hierarchy of directories and their subdirectories along with files. If you dont have the command use sudo apt-get install tree
<img width="1077" height="260" alt="j harison disk" src="https://github.com/user-attachments/assets/d8863127-8fe1-4c0a-bac7-dc856f15a958" />


<img width="1226" height="1056" alt="tree1" src="https://github.com/user-attachments/assets/bc65fbd5-1624-42c1-99cf-1b2840ff37d1" />

<img width="1126" height="865" alt="tree2" src="https://github.com/user-attachments/assets/95d4e46a-b7ed-4197-93eb-620c700b0c4a" />






























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










