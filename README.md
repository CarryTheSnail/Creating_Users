<p align="center">
<img src="https://i.imgur.com/pU5A58S.png" alt="Microsoft Active Directory Logo"/>
</p>

<h1>On-premises Active Directory Deployed in the Cloud (Azure)</h1>
In this part of the project I create 10,000 users using a script on PowerShell.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Active Directory Domain Services
- PowerShell

<h2>Operating Systems Used </h2>

- Windows Server 2022
- Windows 10 (21H2)

<h2>High-Level Deployment and Configuration Steps</h2>

- Step 1: Install Active Directory
  - Login to DC-1 and install Active Directory Services within Server Manager.
- Step 2: Promote as a DC: Setup a new forest as mydomain.com. Restart DC-1 and log back in as user: mydomain.com\labuser
- Step 3: In Active Directory Users and Computers (ADUC), create an Organizational Unit (OU) called "_EMPLOYEES" and "_ADMINS"
- Step 4: Create a new employee named "Jane Doe" and add the user to the "Domain Admins" Security Group
- Step 5: Re-login to DC-1 as "mydomain.com\jane_admin"
- Step 6: Join Client-1 to your domain (mydomain.com). Login to Client-1 as original local admin and join to the domain.
- Step 7: Login to the Domain Controller and verify Client-1 shows up in ADUC
- Step 8: Log into Client-1 as mydomain.com\jane_admin and allow “Domain_Users” access to remote desktop. (System Properties -> Remote Desktop)
- Step 9: Create a bunch of additional users using PowerShell ISE. Attempt to log into client-1 with one of the users. 

<h2>Deployment and Configuration Steps</h2>

Step 1: Install Active Directory. Login to DC-1 and install Active Directory Services within Server Manager.

![image](https://github.com/user-attachments/assets/857cf1b3-2d14-4013-9f0e-781870cfd612)
![image](https://github.com/user-attachments/assets/09be52bc-a229-4967-9e72-db1afaefb5ea)

<br />

Step 2: Promote as a DC: Setup a new forest as mydomain.com. Restart DC-1 and log back in as user: mydomain.com\labuser

![image](https://github.com/user-attachments/assets/f77fa231-1f9e-4f0d-8376-87f351f1848b)
![image](https://github.com/user-attachments/assets/74a7ab20-631b-4aa1-b170-5dfb51b064c2)

![image](https://github.com/user-attachments/assets/b0aa64c6-c7f7-4b18-8aa8-15d313e7a6aa)

<br />

Step 3: In Active Directory Users and Computers (ADUC), create an Organizational Unit (OU) called "_EMPLOYEES" and "_ADMINS"

![image](https://github.com/user-attachments/assets/2b222306-16b2-41e3-98cd-a63763247afd)
![image](https://github.com/user-attachments/assets/710e13f1-de8d-43d2-a71e-a66e3d68d17e)
![image](https://github.com/user-attachments/assets/0ab28879-696f-4b9d-aed1-ffbef07ee0e8)

<br />

Step 4: Create a new employee named "Jane Doe" and add the user to the "Domain Admins" Security Group

![image](https://github.com/user-attachments/assets/8e2df14f-77f8-45df-a0e9-c394e70b76ae)
![image](https://github.com/user-attachments/assets/d8ed1d51-8580-492a-bb28-c69c6e9b0aa8)

<br />

Step 5: Re-login to DC-1 as "mydomain.com\jane_admin"

![image](https://github.com/user-attachments/assets/ec9bb7f8-f082-4f1a-bf48-1f3b2c00cdf5)

<br />

Step 6: Join Client-1 to your domain (mydomain.com). Login to Client-1 as original local admin and join to the domain.

![image](https://github.com/user-attachments/assets/1d9a3a12-1409-48e8-80cd-bc2695727400)

<br />

Step 7: Login to the Domain Controller and verify Client-1 shows up in ADUC

![image](https://github.com/user-attachments/assets/e516d149-0e3d-4feb-8f5b-515420796dcc)

<br />

Step 8: Log into Client-1 as mydomain.com\jane_admin and allow “Domain_Users” access to remote desktop. (System Properties -> Remote Desktop)

![image](https://github.com/user-attachments/assets/2fc3e5fd-0eba-49a2-a178-9389159b7916)

![image](https://github.com/user-attachments/assets/368bbaa6-6846-4009-868a-1b9854b14a52)


<br />

Step 9: Create a bunch of additional users using PowerShell ISE. Attempt to log into client-1 with one of the users. 

![image](https://github.com/user-attachments/assets/862510f5-e2e0-4a1a-835d-f67d58853afe)

![image](https://github.com/user-attachments/assets/c3b3e96b-b45b-41c6-87b1-cb5de43f3b34)

![image](https://github.com/user-attachments/assets/ec66f7fe-1e02-46ac-bfbe-e56be6306861)

![image](https://github.com/user-attachments/assets/8b77bf2c-a593-40ec-aa1b-11cde295c6a2)

![image](https://github.com/user-attachments/assets/3f45afe5-8b48-4e7a-a352-4d00010de2fe)



<br />
