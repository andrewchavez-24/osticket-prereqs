<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10 Pro (22H2), at least 2vCPUs, 8GB RAM

<h2>List of Prerequisites</h2>

- <b>PHP manager for IIS</b> - ensures PHP is correctly configured to run IIS
- <b>Rewrite module </b> - facilitates URL rewriting and redirect users to URLs
- <b>VC_redist.x86</b> (redistributable) - osTicket relies on libraries that are part of Microsoft Visual C++ and ensures the program runs smoothly
- <b>MySQL</b> - for storing data into databases
- <b>HeidiSQL</b> - interface for accessing MySQL 

<h2>Installation Steps</h2>

<p>
Set up a Windows 10 Virtual Machine in Azure and get logged in. Within the VM, download the <a href= https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD>osTicket-Installation-Files.zip</a> and unzip it onto your desktop. The folder should be called “osTicket-Installation-Files”
We will use the files in this folder to install osTicket and some of the dependencies.
</p>
<p>
<img src="https://github.com/user-attachments/assets/f5f62563-9088-4e42-a8f0-e4fe350e9bad" height="80%" width="80%"/>
</p>

<br>
<p>
Install / Enable IIS in Windows WITH CGI
World Wide Web Services -> Application Development Features -> [X] CGI
</p>
<p>
<img src="https://github.com/user-attachments/assets/7dd47789-0fc3-46b7-adb8-7aa328431e32" height="80%" width="80%"/>
</p>

<br />
<p>
From the “osTicket-Installation-Files” folder, install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)
</p>
<p>
<img src="https://github.com/user-attachments/assets/e630afee-033f-4d1b-be7a-b7425ac10290" height="80%" width="80%"/>
</p>

<br />
<p>
From the “osTicket-Installation-Files” folder install the Rewrite Module (rewrite_amd64_en-US.msi)
</p>
<p>
<img src="https://github.com/user-attachments/assets/811178a9-5a5b-4568-825e-de473636d93a" height="80%" width="80%"/>
</p>

<br>
<p>
Create the directory C:\PHP
</p>
<p>
<img src="https://github.com/user-attachments/assets/e0740296-d3ed-4b55-be8f-f089dcd1309d" height="80%" width="80%"/>
</p>

<br>
<p>
From the “osTicket-Installation-Files” folder, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder
</p>
<p>
<img src="https://github.com/user-attachments/assets/2676e90e-6fb2-4de7-a258-2505496144c5" height="80%" width="80%"/>
</p>

<br>
<p>
From the “osTicket-Installation-Files” folder, install VC_redist.x86.exe.
</p>
<p>
<img src="https://github.com/user-attachments/assets/d7f34e08-2a45-4032-9f8e-7ad5e6c72151" height="80%" width="80%"/>
</p>

<br>
<p>
From the “osTicket-Installation-Files” folder, install MySQL 5.5.62 (mysql-5.5.62-win32.msi)
</p>
<p>
<img src="https://github.com/user-attachments/assets/3f05e8cc-d400-4561-9436-ac9c665c88c1" height="80%" width="80%"/>
</p>

<br>
<p>
Open IIS as an Admin
</p>
<p>
<img src="https://github.com/user-attachments/assets/1eb8a134-ec01-4309-860e-1f3395a550d0" height="80%" width="80%"/>
</p>

<br>
<p>
Register PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe)
</p>
<p>
<img src="https://github.com/user-attachments/assets/c98e8a48-527d-4e8f-9f9c-19d0243bd14f" height="80%" width="80%"/>
</p>

<br>
<p>
Reload IIS (Open IIS, Stop and Start the server)
</p>
<p>
<img src="https://github.com/user-attachments/assets/2983064d-e5da-46a3-85d5-d0d807f9dd52" height="80%" width="80%"/>
</p>

<br>
<p>
 Install osTicket v1.15.8
From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” and copy the “upload” folder into “c:\inetpub\wwwroot”
Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket”
</p>
<p>
<img src="https://github.com/user-attachments/assets/27cc30ad-09e4-4b00-a673-31d57ebead2e" height="80%" width="80%"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/b154e9f4-9b74-4daa-a70e-34e1370db132" height="80%" width="80%"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/f6412a44-8790-4326-8a95-a50c3a954582" height="80%" width="80%"/>
</p>

<br>
<p>
Reload IIS (Open IIS, Stop and Start the server)
</p>
<p>
<img src="https://github.com/user-attachments/assets/6d4c46ab-354c-4c34-aead-176acb82eb32" height="80%" width="80%"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/16c81e38-e8a4-4c52-bf8a-5612b2a8d2b8" height="80%" width="80%"/>
</p>

<br>
<p>
Go to sites -> Default -> osTicket
On the right, click “Browse *:80”
</p>
<p>
<img src="https://github.com/user-attachments/assets/1b56533d-778e-48cd-ba71-9de9f8497738" height="80%" width="80%"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/10e6d159-c776-462b-9fc6-4ef2d67e1224" height="80%" width="80%"/>
</p>

<br>
<p>
Note that some extensions are not enabled
Go back to IIS, sites -> Default -> osTicket
Double-click PHP Manager
Click “Enable or disable an extension”
Enable: php_imap.dll
Enable: php_intl.dll
Enable: php_opcache.dll
Refresh the osTicket site in your browser, observe the changes
</p>
<p>
<img src="https://github.com/user-attachments/assets/b5a8b65f-cd67-46e4-a5fa-c6f761f81170" height="80%" width="80%"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/807ee8a5-5a55-4954-802e-b082668240f2" height="80%" width="80%"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/1468494d-9cf8-4f6b-ad14-64d800e762a8" height="80%" width="80%"/>
</p>

<br>
<p>
Rename: ost-config.php
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
To: C:\inetpub\wwwroot\osTicket\include\ost-config.php
</p>
<p>
<img src="https://github.com/user-attachments/assets/948c6888-072a-434e-aaf0-167cee1a653a" height="80%" width="80%"/>
</p>

<br>
<p>
Assign Permissions: ost-config.php
Disable inheritance -> Remove All
New Permissions -> Everyone -> All
</p>
<p>
<img src="https://github.com/user-attachments/assets/a09d8b4e-7338-4e3c-b6a4-9dc4c4884e5a" height="80%" width="80%"/>
</p>

<br>
<p>
Continue Setting up osTicket in the browser (click Continue)
Name Helpdesk
Default email (receives email from customers)
</p>
<p>
<img src="https://github.com/user-attachments/assets/307a5c88-2da0-48e4-b6cc-a01c0e3bc9a5" height="80%" width="80%"/>
</p>

<br>
<p>
From the “osTicket-Installation-Files” folder, install HeidiSQL.
Open Heidi SQL
Create a new session, root/root
Connect to the session
Create a database called “osTicket”
</p>
<p>
<img src="https://github.com/user-attachments/assets/bba50f48-722c-475d-949a-0236ac197bb0" height="80%" width="80%"/>
</p>
<p>
<img src="https://github.com/user-attachments/assets/98a4a751-6b50-4bd1-8746-00f5c9ddff30" height="80%" width="80%"/>
</p>

<br>
<p>
Continue Setting up osTicket in the browser
MySQL Database: osTicket
MySQL Username: root
MySQL Password: root
Click “Install Now!”
</p>
<p>
<img src="https://github.com/user-attachments/assets/e4f0f4a2-e496-4609-80e1-f6497bafbaf7" height="80%" width="80%"/>
</p>

<br>
<p>
You should now see the page telling you that osTicket is finally installed and the links to login into the osTicket as a general user (http://localhost/osTicket) or as staff (http://localhost/osTicket/scp).
</p>

<p>
<img src="https://github.com/user-attachments/assets/73124a65-eaf8-4cef-9f10-6b5767c94b21" height="80%" width="80%"/>
</p>

<h2>osTicket Installed!</h2>

<b>osTicket is now installed and ready for use! In the next project I will walk you through how to configure osTicket!  </b>
<br />
<br />
</p>
