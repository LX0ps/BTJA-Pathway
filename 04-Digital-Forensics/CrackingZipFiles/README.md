# Intro 

This course is about password protecting zip files and then cracking them using brute-force and dictionary attacks.

# Cracking ZIP Files Activity and Quiz

1. We lauch kali vm and download the file.
2. Unzip it and name it SBT_Steg_Lab.
3. We navigate to the correct path.

<img width="1184" height="189" alt="navigate to sbtzipcrac" src="https://github.com/user-attachments/assets/cbd33256-f6a7-48ad-b88d-7886825b2a7c" />

Q1. What is the working password to unlock BruteForceAttack.zip?
We run the command fcrackzip -b -u BruteForceAttack.zip but its talking a lot of time to crack it. We use a variation of it fcrackzip -b BruteForceAttack.zip -u -c a1 -l 6 

<img width="1273" height="301" alt="brute force taking lot of time" src="https://github.com/user-attachments/assets/6e190228-ee62-4176-b1cf-9c47460101f4" />

<img width="936" height="341" alt="variation brute force" src="https://github.com/user-attachments/assets/7cae9b4c-cb59-4864-b0f3-5933141585f3" />

Here's a breakdown what the command mean:

- fcrackzip: The utility tool itself, designed specifically to find passwords for encrypted ZIP archives.
- b: Stands for Brute-Force mode. Instead of using a predefined wordlist dictionary, the tool programmatically generates and tests every mathematical combination.
- BruteForceAttack.zip: The target file that you are attempting to crack.
  
- -u : This makes sure fcrackzip actually tries to unzip the file, without this we won’t actually get the right password.
- -c a1: Specifies the Character Set the tool is allowed to use for guessing: a: Includes lowercase letters (a–z), 1: Includes numeric digits (0–9).
- Combined (a1), it tells the tool to only use lowercase letters and numbers (alphanumeric, lowercase only).
- -l 6: Sets the Password Length to look for. In this case, it restricts the search to passwords that are 6 characters long.

Dictinary attack way faster: we get the password  **a1b3c5** way faster.

- fcrackzip: The tool used to crack encrypted ZIP archives.

-D: Stands for Dictionary mode. This tells the tool to read passwords line-by-line from an external text file (wordlist) rather than trying to guess them mathematically.

-p /usr/share/wordlists/rockyou.txt: Specifies the path to the password wordlist.

/usr/share/wordlists/rockyou.txt points to RockYou, which is one of the most famous and comprehensive password lists in cybersecurity and digital forensics. It contains millions of real-world passwords leaked from historical data breaches.

-u: Stands for Use Unzip. Just like in the previous command, it attempts to actually decompress a file inside the archive using unzip to verify if a tested password is correct, eliminating false positives.

BruteForceAttack.zip: The target file being attacked. (Even though the filename says "BruteForceAttack", the method being used here is a dictionary attack).



<img width="1157" height="158" alt="dictionary attack way faster" src="https://github.com/user-attachments/assets/bcf69d36-0b62-42bb-8807-b6888678bbc9" />


Q2. What is the working password to unlock DictionaryAttack.zip?

Using the same method from above, the password is FRIENDSHIPSTARS

<img width="1205" height="377" alt="dc attack in the da zip file" src="https://github.com/user-attachments/assets/a9cec048-ba10-4e3b-8f4f-9f86e8c34c9b" />

Q3. What is the text string inside FLAG1.txt?

After unzipping BruteForceAttack.zip with the code a1b3c5 we find the flag1.txt file and use cat to find the string inside it: J201AKKLO

<img width="1100" height="736" alt="flag1" src="https://github.com/user-attachments/assets/f0c22779-229f-4169-a1a4-2dbde5bb0fda" />

Q4.  What is the text string inside FLAG2.txt?


After unzipping DictionaryAttack.zip with the code FRIENDSHIPSTARS we find the flag2.txt and use cat to find the string inside it: 91MD0QL11
<img width="1172" height="562" alt="flag2" src="https://github.com/user-attachments/assets/e5221cfc-7635-4d9c-acac-85751f46007e" />




# Resources 
- https://medium.com/@rajendraprasanth/password-cracking-using-kali-67e0b89578df
- https://elearning.centri.org/home/courses/free-courses/introduction-to-digital-forensics#content#cracking-zip-files#cracking-zip-files#cracking-zip-files-activity-and-quiz-walkthrough
  














