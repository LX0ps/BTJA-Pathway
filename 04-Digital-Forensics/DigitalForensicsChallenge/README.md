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






