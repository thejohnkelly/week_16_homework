## Week 16 Homework Submission File: Penetration Testing 1

#### Step 1: Google Dorking


- Using Google, can you identify who the Chief Executive Officer of Altoro Mutual is: Karl Fitzgerald

- How can this information be helpful to an attacker: It can help someone ith targeted attacks such as Whaling, or even in narrowing down usernames wien attempting to gain access to systems.


#### Step 2: DNS and Domain Discovery

Enter the IP address for `demo.testfire.net` into Domain Dossier and answer the following questions based on the results:

  1. Where is the company located: 9725 Datapoint Drive, Suite 100, San Antonio, TX, 78229

  2. What is the NetRange IP address: 65.61.137.64 - 65.61.137.127

  3. What is the company they use to store their infrastructure: Rackspace Backbone Engineering

  4. What is the IP address of the DNS server: 65.61.137.117

#### Step 3: Shodan

- What open ports and running services did Shodan find: 
    Port 80 running TCP and HTTP
    Port 443 running TCP and HTTPS
    Port 8080 running TCP and http_simple_new(?)

#### Step 4: Recon-ng

- Install the Recon module `xssed`. 
- Set the source to `demo.testfire.net`. 
- Run the module. 

Is Altoro Mutual vulnerable to XSS: 

### Step 5: Zenmap

Your client has asked that you help identify any vulnerabilities with their file-sharing server. Using the Metasploitable machine to act as your client's server, complete the following:

- Command for Zenmap to run a service scan against the Metasploitable machine: 
 
- Bonus command to output results into a new text file named `zenmapscan.txt`:

- Zenmap vulnerability script command: 

- Once you have identified this vulnerability, answer the following questions for your client:
  1. What is the vulnerability:

  2. Why is it dangerous:

  3. What mitigation strategies can you recommendations for the client to protect their server:

---
© 2020 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.  

