# 01. Dark Web Operations — Capstone Lab Write-Up

> **Module:** Introduction to Dark Web Operations (Centri / Security Blue Team)  
> **Investigator:** lx0ps  

![Course Completion / Lab Status](completion_cert.png)

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
