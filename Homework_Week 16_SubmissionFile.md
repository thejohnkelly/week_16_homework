## Week 16 Homework Submission File: Penetration Testing 1

#### Step 1: Google Dorking

- Using Google, can you identify who the Chief Executive Officer of Altoro Mutual is: 
      ```
      Karl Fitzgerald
      ```

- How can this information be helpful to an attacker: 
      It can help someone ith targeted attacks such as Whaling, or even in narrowing down usernames wien attempting to gain access to systems.

#### Step 2: DNS and Domain Discovery

Enter the IP address for `demo.testfire.net` into Domain Dossier and answer the following questions based on the results:

  1. Where is the company located: 
        9725 Datapoint Drive, Suite 100, San Antonio, TX, 78229

  2. What is the NetRange IP address:
        65.61.137.64 - 65.61.137.127

  3. What is the company they use to store their infrastructure:
        Rackspace Backbone Engineering

  4. What is the IP address of the DNS server:
        65.61.137.117

#### Step 3: Shodan

- What open ports and running services did Shodan find: 
      Port 80 running TCP and HTTP
      Port 443 running TCP and HTTPS
      Port 8080 running TCP and http_simple_new

#### Step 4: Recon-ng

- Install the Recon module `xssed`. 
      - `marketplace install xssed`
      - `modules load xssed`

- Set the source to `demo.testfire.net`. 
      `options set SOURCE demo.testfire.net`

- Run the module.
       `run`

Is Altoro Mutual vulnerable to XSS: 
      Yes!
[Screen Shot 2021-04-15 at 8 30 54 PM](https://user-images.githubusercontent.com/33046751/114958858-7e047080-9e29-11eb-81f5-f1ff570f2f09.png)

### Step 5: Zenmap

Your client has asked that you help identify any vulnerabilities with their file-sharing server. Using the Metasploitable machine to act as your client's server, complete the following:

- Command for Zenmap to run a service scan against the Metasploitable machine: 
      `nmap -sV 192.168.0.10`
 
- Bonus command to output results into a new text file named `zenmapscan.txt`: 
      `nmap -sV -sC -oN zenmapscan.txt 192.168.0.10`
  ![Screen Shot 2021-04-15 at 9 46 40 PM](https://user-images.githubusercontent.com/33046751/114964362-2f100880-9e34-11eb-8ea5-b2f21eef95f0.png)

- Zenmap vulnerability script command:
      `nmap --script smb-enum-shares 192.168.0.10`

- Once you have identified this vulnerability, answer the following questions for your client:
  1. What is the vulnerability: 
        Anonymous users have read/write privileges

  2. Why is it dangerous:
        If malicous actors gain access to the system they can take advantage of the read/write privileges using the open ports to insert worms and execute ransomware attacks.

  3. What mitigation strategies can you recommendations for the client to protect their server:
        Restrict read/write proviliges only to registered users who require such privileges, use password protection to ristrict use system users who need access, and filter ports to restrict ourside access.

---
© 2020 Trilogy Education Services, a 2U, Inc. brand. All Rights Reserved.  

