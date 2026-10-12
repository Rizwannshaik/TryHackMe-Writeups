
<img width="1654" height="391" alt="Screenshot 2026-10-12 at 20 38 03" src="https://github.com/user-attachments/assets/b73cc314-aa8a-40d6-83ae-b4b428887732" />


## 1. Objective & Scope

This write-up covers the foundational concept of the intro to offensive security. where we will test the security of FakeBank's systems explored in the TryHackMe Pre-Security path. The room serves as a practical introduction to the mindset of an ethical hacker, demonstrating how unauthorized access is achieved through web application exploitation and how to think like an attacker to defend systems better.


# 1.1 TASK 1 - Think like a Hacker!

In this task, there are two security professionals Sarah (Red-Team) & Mike (Blue-Team) working with FakeBank corporation. Sarah is testing logins into the bank's website using common passwords on a test account, to see whether it accepts weak ones. Mike is adding firewall rules that prevent suspicious login attempts on their systems.

Q. Which person is doing offensive security? 

A. Obviously the one who is testing common passwords on bank's website. Hint: "S". 

# 1.2 TASK 2 - Starting the Lab. 

A fake banking application called FakeBank will launch. When the lab loads, you'll see the banking application running in your browser on the right, showing Mrs G. Benjamin's banking account.

<img width="1594" height="869" alt="image" src="https://github.com/user-attachments/assets/3061880d-5462-4cae-bc2f-dafc7ff3af75" />

Q. What is the bank account number shown in the FakeBank application?

A. 8881 (can be seen in website) 

# 1.3 TASK 3 - Finding Hidden Pages. 

In this task, we need to find hidden/sensitive subdomains of the TLD. We are using Dirb (Subdomain enumerator) for this task on FakeBank's website. 

Usage: dirb http://example.com 

<img width="565" height="96" alt="Screenshot 2026-10-12 at 20 48 19" src="https://github.com/user-attachments/assets/13bd930a-9de9-4bf8-afbe-56e5533e160f" />

Q. Dirb found two URLs, which one of these is more likely to give us access to FakeBank's internal tools?

A. Can be retrieved once scan is completed. 
 
# 1.4 TASK 4 - Attack the Admin Page. 

To navigate to this hidden admin panel, we will add this newly discovered page to the search bar located at the top of the website. To do so, you will need to add the following: /bank-transfer. It looks like we can deposit money into Mr's G.Benjamin's account using this admin panel. Test this by selecting the account number you verified in task 2 (8881) and depositing at least 2,000 until your balance turns positive.

<img width="785" height="716" alt="Screenshot 2026-10-12 at 20 54 49" src="https://github.com/user-attachments/assets/2ac7a053-08e6-4c6a-8b2c-47e8c13ad26d" />

Q. What could FakeBank do to make this bank-transfer page secure? Pick the most effective technique:

Require login
Make the URL harder to guess
Move the page to another server

A. Require Login. 

Q. When Mrs. G Benjamin's account balance turns positive, a pop-up with green text appears.

A. <img width="832" height="671" alt="Screenshot 2026-10-12 at 20 56 28" src="https://github.com/user-attachments/assets/c002dafe-decc-4d08-b208-440b999cfcf4" />



