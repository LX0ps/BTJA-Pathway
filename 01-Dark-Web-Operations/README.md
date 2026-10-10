# 01. Dark Web Operations — Capstone Lab Write-Up

> **Module:** Introduction to Dark Web Operations (Centri / Security Blue Team)  
> **Investigator:** lx0ps

1) **What command is used in the Console to generate valid credentials? Provide the credentials, too.**

Before we load Tor we use a vpn for secure connection. Then we go to the onion link provided and we land on the site the image is showing. We then right-click go on inspect and then to console tab and run the command **generateUserCredentials()**
We take the Base64 credential and we use cyberchef to decode it using the from base64 recipe.
From this we get the credential the username and the password.


<img width="965" height="488" alt="darkweb" src="https://github.com/user-attachments/assets/b4f3b38d-ca2d-4ead-9d34-fe78c4443a67" />

<img width="982" height="527" alt="darkweb2" src="https://github.com/user-attachments/assets/44d25314-b88b-4ebf-8497-96539f77ae5d" />

<img width="952" height="400" alt="darkweb3" src="https://github.com/user-attachments/assets/362e0039-76e7-43e6-8e6e-b5440c09ccf1" />

<img width="997" height="376" alt="credentials" src="https://github.com/user-attachments/assets/0c50ed47-3d07-4b66-8ef3-2be7d2032568" />



2) **After logging in, what are the titles of the three pinned posts seen on the website in ASCII text? Please place them in respective order.**

We go and look at the 3 posts and take their hex values and decode them using cyberchef.

<img width="989" height="401" alt="decode images" src="https://github.com/user-attachments/assets/5a06d37a-844d-4b16-a8a6-1462bc7d1cf0" />
<img width="994" height="373" alt="cyber2" src="https://github.com/user-attachments/assets/d8e2767c-e8b2-4dfa-9786-933ccb15fc5d" />

From cyberchef we get in order: **Drugs**, **Pleasure**, and **Drops** from the decoded ASCII text.



3) **Look at the Messages board. They are mentioning another illegal site. Provide its name.**

We go down the message board and we find user **Basilisk95** and click on the hyperlink , this leads us to another site from hacking group **Midnite**.

<img width="983" height="213" alt="q3" src="https://github.com/user-attachments/assets/a293b6fd-3b34-4748-9aa3-2ce54832d0f2" />

<img width="963" height="516" alt="md" src="https://github.com/user-attachments/assets/bf54d612-6c7e-47a2-aebb-958af0b30c42" />


4) **A transaction log is mistakenly visible under the “Recent Transactions” section. Provide the customer’s full name, email address, and the purpose of the transaction.**

We go down to recent transactions and click on the $7000 hyperlink text. We get an invoice to view.

<img width="943" height="145" alt="q4" src="https://github.com/user-attachments/assets/9a40468a-3bd3-480f-b80a-778a77f25b44" />

<img width="971" height="492" alt="transaction" src="https://github.com/user-attachments/assets/5e6c6162-3bea-435a-97ff-972b772b8c30" />


5) **It looks like the user PJ is hosting an illegal party. What city is this taking place and when? We could catch him there and shut down this entire operation.**

We download the image from PJ post and decode it using this site https://stylesuxx.github.io/steganography/. After that we get a riddle to solve, leading to the city of Cardiff.

<img width="931" height="505" alt="q5" src="https://github.com/user-attachments/assets/110f9d49-92d5-4fbb-b726-945706a42fbe" />

<img width="973" height="404" alt="q52" src="https://github.com/user-attachments/assets/697d79f1-72e6-4dce-a739-5a8e6e00921f" />

<img width="678" height="302" alt="q53" src="https://github.com/user-attachments/assets/3a071005-5410-4593-ac75-3194e2e20248" />

<img width="526" height="315" alt="q54" src="https://github.com/user-attachments/assets/affb1b46-cbea-4b59-a3b4-1b33865293bc" />


6) **What is the email of the user selling ‘stolen’ car parts?**

We go to the post with the car image and decode the hexadecimal string within the message. This will give us the user's email address.


<img width="944" height="498" alt="q6" src="https://github.com/user-attachments/assets/3975abcc-4b51-4ea9-a3b3-6a45adab6f64" />

<img width="984" height="490" alt="q61" src="https://github.com/user-attachments/assets/95e5af1b-5fb2-4847-9b25-890f62220ee8" />










---
 

## 🎯 Mission Scenario
Authorities recently dismantled a major drug trafficking network operating through the TOR network. However, a key creator evaded capture and migrated to a personal hidden service blog—disguised under harmless topics like chocolate—to continue illicit coordination. 

**Objective:** Investigate the hidden service, uncover evidence linking the individual to drug trafficking, identify the suspect, and locate details regarding an upcoming illicit shipment for interdiction.

---

## 📋 Capstone Challenge Solutions & Findings

| Challenge Question | Investigation Result / Answer |
| :--- | :--- |
| **1. Initial Access Credentials** | Username: `KF7ybuD1` <br> Password: `AlyhfotoV9VIWm6W` |
| **2. Suspect's Site Username** | `Darkchest984` |
| **3. Suspect's Full Name** | Kestner Richard |
| **4. Suspect's Current Country** | United Kingdom (UK) |
| **5. Encoding Format Used** | Hexadecimal / Base64 |
| **6. Target Seaport & Delivery Location** | Port of Felixstowe, England (`51° 56' 57.2"N 1° 19' 26.1"E`) |
| **7. Upcoming Shipment Date** | `31/10/20XX` |

---

## 🛠️ Step-by-Step Investigation Methodology

### Phase 1: Tor Access & Credential Extraction
* **Environment Setup:** Connected securely to the Tor network using recommended operational security precautions.
* **Authentication Bypass:** Navigated to the hidden service login prompt. Using browser developer tools (`Inspect Element` $\rightarrow$ `Console`), executed the target script function `generateUserCredentials()` to pull obfuscated access tokens.
* **Decoding:** Analyzed and decoded the extracted Base64/Hexadecimal strings to successfully log into the restricted dashboard.

### Phase 2: Content Analysis & Reconnaissance
* Explored the hidden blog posts masking as a specialty chocolate page.
* Identified alternate hidden sections pointing to high-risk illicit markets (recreational drugs, contraband firearms, and restricted documents).
* Extracted historical timestamps from blog entries to chart the suspect's operational timeline.

### Phase 3: OSINT, Attribution & Geolocation
* **Image Forensics:** Performed reverse image searches on target profile imagery. Utilized image enhancement tools on low-resolution graphics to reveal a US passport and identification details confirming the suspect (`Kestner Richard`).
* **Coordinates & Logistics:** Analyzed a physical "Don't Forget" reminder note containing GPS coordinates (`51° 56' 57.2"N 1° 19' 26.1"E`). Correlated these coordinates with global maritime data to pinpoint the Port of Felixstowe as the entry point for the upcoming `31/10/20XX` shipment.

---

## 💡 Key Takeaways & Defense Insights
* **Browser Console Inspection:** Threat actors often hide interactive hooks or clues in client-side scripts; knowing how to leverage developer tools is vital for blue teamers analyzing rogue portals.
* **OSINT Attribution:** Combining metadata analysis, reverse image enhancement, and coordinate correlation allows investigators to bridge anonymous digital footprints back to physical reality.
