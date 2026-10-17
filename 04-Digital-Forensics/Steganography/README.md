#  Intro to Steganography

“The practice of concealing messages or information within other non-secret text or data.” An example of this would be having a text file that contains secret information, which is hidden inside an innocent image file. 

# Steganography Activity and Quiz

Q1. Embed the file 'secretmessage.txt' inside the cover file 'coverfile.jpg' and name the output stegofile 'hiddenmessage.jpg'. What is the full command you would use to do this?
- steghide embed -ef secretmessage.txt -cf coverfile.jpg -sf hiddenmessage.jpg

1. We launch kali linux vm and download the file SBT_Steg_Lab.
2. We unzip the file and replace the name with SBT_Steg_Lab.
3. We navigate to cd Downloads cd SBT_Steg_Lab.

<img width="999" height="208" alt="navigate to steg lab" src="https://github.com/user-attachments/assets/a0ee2fcb-cad5-45bb-bfd8-b3db5265ae51" />

4. We use the command ls -a to list all files and directories even the hidden ones.

<img width="1190" height="230" alt="hidden files steg" src="https://github.com/user-attachments/assets/61216162-94c2-4a75-942d-3329cd2cb12e" />

5. We run the command steghide embed -ef secretmessage.txt -cf coverfile.jpg -sf hiddenmessage.jpg to embed the file secretmessage.txt inside the cover file coverfile.jpg and name the output stegofile hiddenmessage.jpg.

<img width="1268" height="231" alt="steghide" src="https://github.com/user-attachments/assets/fce97eb6-22e3-42b6-82f4-f93a8f793d24" />



Q2. Flag 1 is hidden inside a text file in one of the steganography files. What is the value? 
- kAN105KS

We change directories into the Stego Files folder. 
<img width="1273" height="396" alt="stego files" src="https://github.com/user-attachments/assets/2c075ebb-60e0-4766-98e6-a829a1b2d606" />

The flag is in the pizza.jpg file 

<img width="1391" height="496" alt="flag1" src="https://github.com/user-attachments/assets/80db6899-fc32-4ce1-a030-1f23b8b5324b" />


Q3.  Flag 2 is hidden inside a text file in one of the steganography files. What is the value?
- 001JDANL

<img width="1340" height="613" alt="flag2" src="https://github.com/user-attachments/assets/0eb9dac1-c158-4404-a657-dd0bc1f3b7b5" />

Q4.  Flag 3 is hidden inside a text file in one of the steganography files. What is the value?

- 1LRBA9IU

<img width="1305" height="506" alt="flag3" src="https://github.com/user-attachments/assets/2cdb8030-0476-4316-b008-c25b1893850b" />














