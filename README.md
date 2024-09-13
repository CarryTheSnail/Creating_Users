<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
In this part of the project I create 10,000 users using a script on PowerShell.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- Group Policy Management Console

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Part 1: Configure Group Policy to Lockout the accounts after 5 attempts.
- Part 2: Dealing with Account Lockouts
- Part 3: Enabling and Disabling Accounts
- Part 4: Obsering Logs

<h2>Configure Group Policy to Lockout the account after 5 attempts:</h2>

Step 1: Open Group Policy Management Console (GPMC) 

![image](https://github.com/user-attachments/assets/6ca4d725-5a58-48e2-867e-df31490c32c4)

![image](https://github.com/user-attachments/assets/34cb3267-f4a8-4c9a-bbf3-1b0470ed7b1e)

Step 2: Edit a Group Policy Object so that User Accounts are locked after 5 incorrect password attempts. (In this case, I used the Default Domain Policy for mydomains.com. Navigate to the Account Lockout Policy Settings. Configure Account Lockout Policy Settings. (Computer Configuration > Policies > Windows Settings > Security Settings > Account Policies > Account Lockout Policy)

![image](https://github.com/user-attachments/assets/c9d11680-ae26-4df8-a1d1-fb53099965a4)

![image](https://github.com/user-attachments/assets/f2c7b4df-6bb3-4e4d-9405-39bae35ca62d)


Step 3: Update Group Policy: Command Prompt and type gpupdate /force 
(make sure to use admin user account) 

![image](https://github.com/user-attachments/assets/67c01346-7f85-4394-b5b4-b58a855825d5)


<br />

<h2>Dealing with Account Lockouts</h2>

Step 1: Pick a random user account you created previously. Attempt to log in with 6 incorrect password attempts. 

![image](https://github.com/user-attachments/assets/9ad67446-b959-4ae9-87d9-612e406cb588)

![image](https://github.com/user-attachments/assets/ca6c879d-d39a-43ad-8bc0-d3cf0c305b13)

![image](https://github.com/user-attachments/assets/43aa6850-4bcb-4022-b58d-ba16ce49bb81)


Step 2: Observer that the account is locked out from Active Directory. Unlock the account. Reset Password.
 
![image](https://github.com/user-attachments/assets/d0698797-6b2e-46c2-b00e-c3072e207151)



Step 3: Attempt to login to the unlocked account. 

![image](https://github.com/user-attachments/assets/becf86f3-8a03-415f-84f4-844bf2f074f7)

![image](https://github.com/user-attachments/assets/3ba76ba6-7b9b-46d4-a0f2-047bd47d616d)

![image](https://github.com/user-attachments/assets/f7bd8bbc-5386-426c-acf2-4a036f95e4cf)

<br />

<h2>Enabling and Disabling Accounts</h2>

Step 1: Search for the account by username in Active Directory

![image](https://github.com/user-attachments/assets/b7bb7f42-51fc-4932-8151-6f551a9cd937)

Step 2: Disable the account in Active Directory

![image](https://github.com/user-attachments/assets/a67dbb94-140b-4589-8cdf-47f090fbcb51)

Step 3: Try logging into the disable user account and observe the error message notifying that the account has been disabled.

![image](https://github.com/user-attachments/assets/960dcd75-a58a-4126-b9bf-1e0b126eeaa5)

Step 4: Enable the disabled account

![image](https://github.com/user-attachments/assets/395494b0-e3d0-4a10-81b5-2409a5958b6f)
![image](https://github.com/user-attachments/assets/81a23744-e16d-46cd-b48f-6cd3b249364d)

<h2>Observing Logs</h2>

Step 1: Use Event Viewer to observe logs

![image](https://github.com/user-attachments/assets/d76613f2-6e04-4d94-82c2-016f17a5edfc)

Step 2: Search for the user account that was used (fox.civ)

![image](https://github.com/user-attachments/assets/e61921ef-1a3a-44de-99db-2ee9fb8685d8)

Step 3: Observe the Audit Failure from failed login attempts 

![image](https://github.com/user-attachments/assets/27fa6955-1160-4d5a-a707-97f7edb456c6)




