# Intro 

Google Dorks are search hacks where we can use special arguments in a normal Google query to find specific information. Dorks come in the format operator:keyword, an example of this would be filetype:pdf. Real-world examples of using Dorks include:

- Retrieving files from domains.
- Finding hidden web pages and login portals.
- Subdomain enumeration.
- And more.

# Finding Files

We search in google **Cyber Security filetype:pdf** so we can get results for pdf files containing the keyword Cyber Security 

<img width="1188" height="970" alt="google dorks" src="https://github.com/user-attachments/assets/76fdbefd-86bf-4649-8576-7dc72adb94a2" />


# Subdomain Enumeration 

We use Dorks to enumerate all subdomains of a domain, for passive reconnaissance purposes. For this, we will use Facebook again as the example, with the following query: site:Facebook.com -site:www.Facebook.com

<img width="1219" height="968" alt="sub enu" src="https://github.com/user-attachments/assets/08aaeb4a-9f08-4723-a4be-370b9c59ca00" />


# Keyword Searching 

Using the Dork inurl: (value) we can look for specific keywords in a much more refined way than normal google searches. Using the query inurl: admin we can see a number of what appears to be admin login portals. This would be great if we were working as an attacker (if in scope, we can brute force or bypass the login portal to access administrator dashboards) or a defender (we can work to secure these portals so they are not compromised).

<img width="1335" height="978" alt="new" src="https://github.com/user-attachments/assets/0af308e2-8a74-4fbd-9bd0-b2c386c2a353" />


# Resources 

- https://elearning.centri.org/home/courses/free-courses/introduction-to-osint#content#tools-and-services#tools-and-services#google-dorks










