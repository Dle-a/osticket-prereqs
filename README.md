<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />



- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Enabled IIS internet information services
- Installed web platform installer
- Installed MSQL and setup username and password 
- Installed C++ redistributable 
- Installed Osticket and enabled permissions

<h2>Installation Steps</h2>
 The first is to create a virtual machine by going to https://portal.azure.com/. Setup your virtual machine with Windows 10 Pro, version 22H2. Note, create a virtual machine with atleast 2 vcpus and 16 gbs of memory.

 Conncet to the VM by using the public ip address the vm is setup with. You will connect using the remote desktop connection app.


![image](https://github.com/user-attachments/assets/38e9aa99-7aa9-4265-887c-6346f3772ca2)


<img width="305" alt="image" src="https://github.com/user-attachments/assets/3e829718-c94e-41c8-b3af-599facad753d" />



 Once you have connected to your VM go to the control panel, from the control panel open up programs. Select, Turn Windows features on and off.
 
 ) install / enable IIS in Windows with CGI and Common HTTP Features,
install PHP Manager for IIS (PHPManagerForIIS_V1.5.o.msi)
install the Rewrite Module (rewrite_amd64_en-US.msi)

Create a new folder directory C:\PHP, From the “osTicket-Installation-Files” folder, install VC_redist.x86.exe.

Download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi) from the installation files. Within the MySQL setup wizard, click "I agree" and select a Typical install and Install. Launch the Configuration Wizard after the installation. Select Standard Configuration and select Install As Windows Service and make sure Launch the MySQL Server automatically is checked. For credentials, the username will be root and the password is Password1. In a practical setting, the credentials will be basic to where they can be easily guessed. For the purposes of this lab, the standard credentials root and Password1 will do.

<img width="182" alt="image" src="https://github.com/user-attachments/assets/e4d66af6-9a93-4095-95db-80ac6c727ca3" />

Open IIS as an Admin, register PHP from with IIS(PHP Manager -> C:\PHP\php-cgi.exe)

From the installation files, download osTicket v1.15.8. Extract and copy the "upload" folder to the following path: c:\inetpub\wwwroot. Within the c:\inetpub\wwwroot folder, rename "upload" to "osTicket." Reload the IIS server afterwards.
<img width="488" alt="image" src="https://github.com/user-attachments/assets/ab12b610-a93f-4e5f-a280-2560065e7104" />






5.)



9.)

Next, download and install MySQL 5.5.62 (mysql-5.5.62-win32.msi) from the installation files. Within the MySQL setup wizard, click "I agree" and select a Typical install and Install. Launch the Configuration Wizard after the installation. Select Standard Configuration and select Install As Windows Service and make sure Launch the MySQL Server automatically is checked. For credentials, the username will be root and the password is Password1. In a practical setting, the credentials will be basic to where they can be easily guessed. For the purposes of this lab, the standard credentials root and Password1 will do.



<img width="161" alt="image" src="https://github.com/user-attachments/assets/61209dfa-9425-472f-817e-361dbb8e2241" />

<p>
<img width="727" alt="Annotation 2025-02-11 140738" src="https://github.com/user-attachments/assets/bda1ba45-4bbc-42de-bf21-52f65d7ca0a4" />
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img width="632" alt="Annotation 2025-02-11 134000" src="https://github.com/user-attachments/assets/13bda1b6-cc3f-4e0f-a36d-13553100b986" />
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />

<p>
<img width="711" alt="Annotation 2025-02-11 034549" src="https://github.com/user-attachments/assets/ed60c7b4-eb96-453c-a60a-47c6d5a5ec1e" />
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
