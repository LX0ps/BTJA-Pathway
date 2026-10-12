# Challenge Scenario and Details

You work for a law enforcement organisation, and you have been assigned to track a person-of-interest, that is believed to be associated with a hacking group that recently compromised a Managed Service Provider (MSP) and are trying to sell the stolen credentials on both the clear net and dark web. Another team is focusing on the dark web lead, so you have been tasked with using OSINT sources to build up a profile on the individual and attempt to locate any evidence that links them to the MSP breach and sale of account details. You have been provided with some information to start your investigation. You should use any of the sources or tools taught in this course, that you deem to be applicable and appropriate. We know that the email address used to register the Twitter account is fake, so do not include this in your report.

Your manager has provided you with the following starting information:

 - Twitter handle used by actor: @sp1ritfyre

<img width="949" height="1003" alt="report" src="https://github.com/user-attachments/assets/45c9c1ae-a5b6-4ec3-bc25-208a22bcf8d0" />

Using the Google search allintext:sp1ritfyre we find that there is an X account with that name 

<img width="1099" height="829" alt="x account" src="https://github.com/user-attachments/assets/76c5b827-24ce-4d7f-8f05-e35d657059c2" />



We find a message link in the profile and use cyberchef to decode it 

<img width="1290" height="744" alt="cyberchef" src="https://github.com/user-attachments/assets/71cbb8eb-a3bd-425d-b1ba-6bf25b534570" />

We got the link redhunt.net


We didnt get any info from the site we search the name "sp1ritfyre" which leads us to this blog website.

<img width="1418" height="835" alt="sp1ritfyre" src="https://github.com/user-attachments/assets/95abad41-abab-4069-b9e6-207d9d9bb97c" />

The blog profile immediately give us valuable information so we can find the target's identity:

- gender: female
- porfile: account active since march 2020
- location: 68747470733a2f2f73616d6d6965776f6f647365632e626c6f6773706f742e636f6d
- Profile views: 40,527


We click on the email and get the d1ved33p@gmail.com 
Now we need to decode the location using cyberchef

<img width="1503" height="736" alt="cyber" src="https://github.com/user-attachments/assets/75ab6535-ed62-4bda-bae5-4b7c199e74dc" />

We get the decoded url: https://sammiewoodsec.blogspot.com/ and find a lot of useful information so we can answer the questions 

<img width="1744" height="972" alt="sammie" src="https://github.com/user-attachments/assets/bd1fbfc6-d21f-44fc-8d12-dc261e648d2c" />


<img width="1272" height="856" alt="sammie2" src="https://github.com/user-attachments/assets/a4404016-28c2-4c0e-96e9-313c7571291b" />

We get from the blog the following info: 

- Name: Sam
- Age: 23
- Education: Studied ICT in college before earning a 1st-class degree in Cyber Security and Forensics from the University of Plymouth.
- Current Employer: PhilmanSecurityInc.
- Role: Junior Pen tester.
- Colleagues/Mentors: Mentions Zach and Dave as mentors at her firm.

# Questions 

1. What is the hacker’s first name?  Sammie
2. What is the hacker’s last name? Woods
3. What is the hacker’s age? 23
4. What country does the hacker live in? United Kingdom
5. What are some of the hacker’s interests? Security, Gaming, Photography, Camping, Malware Analysis
6. What company does the hacker work for? PhilmanSecurityInc
7. What is the hacker’s position within the company? Junior Penetration Tester
8. What is the full url of the website owned by the hacker? https://redhunt.net
9. List any full URLs of websites not owned, but used by the hacker (Blogs only) https://sammiewoodsec.blogspot.com/ https://sp1ritfyrehackerstories.blogspot.com/
10. What email address has been used by the hacker? d1ved33p@gmail.com















