## Week 16 Homework Submission File: Penetration Testing 1

#### Step 1: Google Dorking


- Using Google, can you identify who the Chief Executive Officer of Altoro Mutual is:
`intitle:Chief Executive Officer of Altoro Mutual` **Karl Fitzgerald**
- How can this information be helpful to an attacker:
 **The first step of the Cyber Chain Link is Reconnaissance. A hacker can gather as much information of their target**

#### Step 2: DNS and Domain Discovery

Enter the IP address for `demo.testfire.net` into Domain Dossier and answer the following questions based on the results: 

  1. Where is the company located: 
      - San Antonio, TX
  2. What is the NetRange IP address:
      - 65.61.137.64 - 65.61.137.127
  3. What is the company they use to store their infrastructure:
      - Rackspace Backbone Engineering
  4. What is the IP address of the DNS server:
      - 117.137.61.65
#### Step 3: Shodan

- What open ports and running services did Shodan find:
    - port 80, 443, and 8080
    - Apache Tomcat/Coyote JSP engine version 1.1
#### Step 4: Recon-ng

- Install the Recon module `xssed`. 
- Set the source to `demo.testfire.net`. 
- Run the module. 

Is Altoro Mutual vulnerable to XSS: 
  - unsure kept getting this error
  
### Step 5: Zenmap

Your client has asked that you help identify any vulnerabilities with their file-sharing server. Using the Metasploitable machine to act as your client's server, complete the following:

- Command for Zenmap to run a service scan against the Metasploitable machine: 
  - nmap -sV 192.168.0.10
- Bonus command to output results into a new text file named `zenmapscan.txt`:

- Zenmap vulnerability script command: 
  - nmap --script smb-enum-shares 192.168.0.10
- Once you have identified this vulnerability, answer the following questions for your client:
  1. What is the vulnerability:
    - Anonymous users have read/write access to their SAMBA shares
  2. Why is it dangerous:
    - anyone can access company files and modify them 
  3. What mitigation strategies can you recommendations for the client to protect their server:
      - update SAMBA server to most current version
---
© 2020 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.  

