# Indicators of Compromise 

Indicators of Compromise, also referred to as IOCs are a method of information sharing, so that organisations can determine whether they have come into contact with similar attacks. These are some examples of common IOCs:

- IP Addresses – If an IP is behaving maliciously, it can be considered an IOC. 
- Email Addresses – If an email address is sending out malicious emails, it can be considered an IOC.
- File Sizes Value – It’s pretty unlikely that a large number of files will have the exact same number of bytes.
- MD5/SHA-1 Hashes – Hashing is a one-way cryptographic function that allows us to create a signature represented by a string value, known as a checksum.
- Strings – We can retrieve strings from a file, and use them as an IOC for searching.

# Quiz Activity

Now that you know how to make IOC files using Mandiant IOC Editor, it’s time to put your new skills to the test! This activity will have you gathering IOCs from a number of files to make sure you understand everything we’ve covered so far. Remember, this is crucial so you can conduct your malware hunt later in the course. Below are the questions you’ll have to answer when you start the quiz, make sure you have your answers ready.

Download the ZIP file containing the four files for analysis below – We suggest you download this to your Kali VM to make use of Linux commands to retrieve MD5 and SHA-1 hashes.

# File Beginning With “1”

1. What is the SHA1 hash value of this file?

We use the command sha1sum 1HIGHLY_MALICIOUS.txt. The SHA1 hash value is 1f221ebaee912b351ec703874f3a0aa8a019dfd9.

<img width="1233" height="243" alt="file beg with 1" src="https://github.com/user-attachments/assets/41fbf92c-aba7-438c-a2f9-2e9b41de96ec" />

<img width="939" height="183" alt="sha1 hash value" src="https://github.com/user-attachments/assets/9e967c31-31cb-4f1c-8888-7f26a69caa6a" />

2. What is the MD5 hash value of this file?

We use the command md5sum 1HIGHLY_MALICIOUS.txt. The MD5 hash value is cf49367f7c184ee0a9ec7bc8c1ba907f.

<img width="955" height="125" alt="md5sum of file 1" src="https://github.com/user-attachments/assets/b4d0bc99-456d-4e71-a576-2aa12938e4a5" />


3. What is the file size (in bytes, with no separators such as “,”) of this file?

So for this one there are a lot of ways to find the size of the file. You can use different commands in cli or just find the file and click properties so you can see the file is 86 bytes. ls -lh filename.txt  or stat filename.txt or find the file properties. We get the same results of 86bytes.

<img width="1226" height="484" alt="file size is 86bytes of the txt" src="https://github.com/user-attachments/assets/381290d3-db81-4dda-889f-e26458d7c13a" />

<img width="366" height="220" alt="another way to find size of file 1" src="https://github.com/user-attachments/assets/e834ed50-e0ef-48d8-9aa8-fd49af85dfc6" />

4. What is the full file name (and extension) of this file?

From the above screenshot we see that the full name of this file is 1HIGHLY_MALICIOUS.txt.


# File Beginning With “2”

We follow the same steps as the above one but for the file  **2innocent.pdf**.
1. What is the SHA1 hash value of this file?
<img width="1221" height="208" alt="file beg with 2 sha1" src="https://github.com/user-attachments/assets/c1e729b2-6283-4e8f-bd00-99e3de533fcb" />

2. What is the MD5 hash value of this file?

<img width="941" height="131" alt="md5sum file 2" src="https://github.com/user-attachments/assets/d9b800b4-ef20-48ab-a7ee-fd75f4bce481" />


3. What is the file size (in bytes, with no separators such as “,”) of this file?
<img width="977" height="285" alt="file size" src="https://github.com/user-attachments/assets/7d727354-9480-46d2-b91f-5970b5f65730" />

<img width="617" height="571" alt="file size 2nd way to find" src="https://github.com/user-attachments/assets/fd04cb8a-eb50-45f9-b659-e5d7ac95ef7a" />


4. What is the full file name (and extension) of this file?

Using the above screenshot the full file name of this file is 2innocent.pdf.

# File Beginning With “3”



















