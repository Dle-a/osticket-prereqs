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

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Azure Virture Machine
- Internet Information Services (IIS)
- PHP Manager
- Rewrite Module
- VC Redist
- MySQL
- Heidi sql
- osTicketv1.15.8
- Link to downloads
https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6
<h2>Installation Steps</h2>

Begin by creating an Azure Virtual Machine Windows 10, 4 vCPUs,log into the VM with Remote Desktop,within the VM (osticket-vm), download the https://driand, connect to the VM with its public ip address using remote desktop. 
---

![Screenshot 2025-02-19 074233](https://github.com/user-attachments/assets/680899fb-8562-4087-a8be-aac72dda136b)
---




![Screenshot 2025-02-10 152623](https://github.com/user-attachments/assets/318ec3d6-da4f-43eb-987f-59a920521bbc)






The files in this folder are needed to install osTicket and some of the dependencies.

Install / Enable IIS in Windows WITH CGI
World Wide Web Services -> Application Development Features -> [X] CGI

![Screenshot 2025-02-19 075739](https://github.com/user-attachments/assets/45b30555-831c-4b64-b982-c010f32dd80b)

From the “osTicket-Installation-Files” folder, install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)

![Screenshot 2025-02-19 085811](https://github.com/user-attachments/assets/bf22c30d-5c74-4463-b2db-32599132cc66)

From the “osTicket-Installation-Files” folder install the Rewrite Module (rewrite_amd64_en-US.msi)

Create the directory C:\PHP

From the “osTicket-Installation-Files” folder, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder

From the “osTicket-Installation-Files” folder, install VC_redist.x86.exe.

From the “osTicket-Installation-Files” folder, install MySQL 5.5.62 (mysql-5.5.62-win32.msi)
Typical Setup ->
Launch Configuration Wizard (after install) ->

<img width="394" alt="Annotation 2025-02-11 022939" src="https://github.com/user-attachments/assets/d9bbe2e1-5fc7-4967-a790-69101d23dae6" />

Open IIS as an Admin

Register PHP from within IIS (PHP Manager -> C:\PHP\php-cgi.exe)

Reload IIS (Open IIS, Stop and Start the server)

Install osTicket v1.15.8
From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” and copy the “upload” folder into “c:\inetpub\wwwroot”
Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket”
<img width="711" alt="Annotation 2025-02-11 034549" src="https://github.com/user-attachments/assets/1afaa8a4-4825-48e5-a0b7-7166bf92a601" />

Reload IIS (Open IIS, Stop and Start the server)

Go to sites -> Default -> osTicket
On the right, click “Browse *:80”

Note that some extensions are not enabled
Go back to IIS, sites -> Default -> osTicket
Double-click PHP Manager
Click “Enable or disable an extension”
Enable: php_imap.dll
Enable: php_intl.dll
Enable: php_opcache.dll
Refresh the osTicket site in your browser, observe the changes

Rename: ost-config.php
From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
To: C:\inetpub\wwwroot\osTicket\include\ost-config.php

Assign Permissions: ost-config.php
Disable inheritance -> Remove All
New Permissions -> Everyone -> All

Continue Setting up osTicket in the browser (click Continue)
Name Helpdesk
Default email (receives email from customers)

From the “osTicket-Installation-Files” folder, install HeidiSQL.
Open Heidi SQL
Create a new session, root/root
Connect to the session
Create a database called “osTicket”
![Screenshot 2025-02-19 084418](https://github.com/user-attachments/assets/062aab19-adde-460d-b609-5276b17f8c38)

Continue Setting up osTicket in the browser
MySQL Database: osTicket
MySQL Username: root
MySQL Password: root
Click “Install Now!”

Congratulations, hopefully it is installed with no errors!
<img width="632" alt="Annotation 2025-02-11 134000" src="https://github.com/user-attachments/assets/e8b5588a-217b-482b-8e11-eea2d8817f0a" />








