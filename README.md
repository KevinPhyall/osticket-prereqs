# osticket-prereqs<p align="center">
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

- Enable Internet Information Services
- Web Platform Installer
- Install C++ Redistributable
- Install MySQL
- Register PHP
- Enable Extenions
- Configure Permissions
- Install HeidiSQL
- Install osTicket In Browser

<h2>Installation Steps</h2>

<p>
<img width="777" alt="image" src="https://github.com/user-attachments/assets/d7856b4f-dd0d-4a65-a55f-86b2c60f28cd" />

</p>
<p>
Within the VM, Download the osTicket-Installation-Files.zip and unzip it onto your desktop. The folder should be called “osTicket-Installation-Files”
</p>
<br />

<p>
<img width="521" alt="image" src="https://github.com/user-attachments/assets/909969fa-7298-46f9-8e66-3356e8256593" />
</p>
<p>
Install / Enable IIS in Windows WITH CGI.   (Control Panel>Uninstall A Program>Turn Windows Features On or Off)
* IIS -> World Wide Web Services -> Application Development Features -> [X] CGI
</p>
<br />

<p>
<img width="525" alt="image" src="https://github.com/user-attachments/assets/10c79c20-a112-4321-aa90-4fbd70a6ebc6" />

</p>
<p>
From the “osTicket-Installation-Files” folder, install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)
</p>
<br />
<p>
<img width="525" alt="image" src="https://github.com/user-attachments/assets/c61e8c33-541a-42b9-a3ba-31e5e952aef6" />

</p>
<p>
From the “osTicket-Installation-Files” folder install the Rewrite Module (rewrite_amd64_en-US.msi)
</p>
<br />

<p>
<img width="525" alt="image" src="https://github.com/user-attachments/assets/e5cca001-d6cb-4331-9556-f97f61535880" />

</p>
<p>
Create the directory C:\PHP
</p>
<br />

<p>
<img width="525" alt="image" src="https://github.com/user-attachments/assets/00bc7bf7-ef69-43e4-9957-85f295e3d193" />

</p>
<p>
From the “osTicket-Installation-Files” folder, unzip PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) into the “C:\PHP” folder
</p>
<br />

<p>
<img width="525" alt="image" src="https://github.com/user-attachments/assets/02639f65-e73b-467a-8122-f4237cba7f7e" />

</p>
<p>
From the “osTicket-Installation-Files” folder, install VC_redist.x86.exe.
</p>
<br />

<p>
<img width="525" alt="image" src="https://github.com/user-attachments/assets/63e04b59-d6d0-43f8-beae-d9bd8deb51a6" />
</p>
<p>
From the “osTicket-Installation-Files” folder, install MySQL 5.5.62 
* Typical Setup ->
* Launch Configuration Wizard (after install) ->
* Standard Configuration ->

</p>
<br />
<img width="525" alt="image" src="https://github.com/user-attachments/assets/e2a650b2-1cc8-479e-9457-1637cb2ac7b0" />
<img width="541" alt="image" src="https://github.com/user-attachments/assets/d389c766-abe7-40e0-a3ec-983c8c58ae5f" />

<p>
Register PHP from within IIS (Click PHP Manager>Register New PHP>…>C:>PHP>php-cgi.exe)
</p>

<img width="628" alt="image" src="https://github.com/user-attachments/assets/8d4f9b14-fa76-45a2-bfa7-48165462eac8" />
<img width="541" alt="image" src="https://github.com/user-attachments/assets/b007b271-a348-4e99-8be3-489150adcb86" />
<img width="541" alt="image" src="https://github.com/user-attachments/assets/2831526f-33f4-446b-97c6-d7e42383dc3d" />
<img width="541" alt="image" src="https://github.com/user-attachments/assets/8f8ab9b8-c6fb-430e-888b-cf4d55200fad" />
<img width="541" alt="image" src="https://github.com/user-attachments/assets/9b072d95-ae8c-4803-b41f-99c6224c76cb" />

<p>
Install osTicket v1.15.8
* From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” and copy the “upload” folder into “c:\inetpub\wwwroot” 
  (GO TO C DRIVE>INETPUB>WWWROOT
* Within “c:\inetpub\wwwroot”, Rename “upload” to “osTicket”
</p>
<br />

<p>
<img width="382" alt="image" src="https://github.com/user-attachments/assets/7405bc36-e2d6-4053-90ca-a67e7d4f1c2e" />
<img width="496" alt="image" src="https://github.com/user-attachments/assets/3bef9e7d-07c0-4fb1-b8fe-880d2657c0a2" />
<img width="438" alt="image" src="https://github.com/user-attachments/assets/fe7819e9-e116-41d3-8e53-a3621cd69a19" />

</p>
<p>
Note that some extensions are not enabled
* Go back to IIS, sites -> Default -> osTicket
* Double-click PHP Manager
* Click “Enable or disable an extension”
    * Enable: php_imap.dll
    * Enable: php_intl.dll
    * Enable: php_opcache.dll
* Refresh the osTicket site in your browser, observe the changes
</p>
<br />

<p>
<img width="572" alt="image" src="https://github.com/user-attachments/assets/4f3f1710-1787-46db-867b-3b0c6b43e5f1" />

</p>
<p>
Rename: ost-config.php
* From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
* To: C:\inetpub\wwwroot\osTicket\include\ost-config.php
</p>
<br />

<p>
<img width="572" alt="image" src="https://github.com/user-attachments/assets/4cabfbaf-19e6-4c59-84d0-d1b4b6553111" />
<img width="572" alt="image" src="https://github.com/user-attachments/assets/113ef231-85af-4b70-8ec2-e3ca1b842c07" />

</p>
<p>
Assign Permissions: ost-config.php (right click>properties>securities>advanced)
* Disable inheritance -> Remove All
* New Permissions -> Everyone -> All (Add>Select Principal>Everyone>Full Control)

</p>
<br />

<p>
<img width="572" alt="image" src="https://github.com/user-attachments/assets/a4342f97-fbf5-4499-891d-fec7a2fdce8b" />
<img width="400" alt="image" src="https://github.com/user-attachments/assets/d69b069f-9651-40ea-8b86-08c0ef6ce909" />
<img width="442" alt="image" src="https://github.com/user-attachments/assets/1dc3695b-22f5-4a29-9e16-0a83891ddb65" />

</p>
<p>
From the “osTicket-Installation-Files” folder, install HeidiSQL.
* Open Heidi SQL
* Create a new session, root/ (password) >root
* Connect to the session
* Create a database called “osTicket” (Right Click Unnamed>Create New>Database

</p>
<br />

<p>
<img width="628" alt="image" src="https://github.com/user-attachments/assets/426433b9-8efd-44c9-9efd-c4bac910361d" />
<img width="628" alt="image" src="https://github.com/user-attachments/assets/55a3a862-8c6d-4a59-9841-02ea59e809fb" />

</p>
<p>
Continue Setting up osTicket in the browser
* MySQL Database: osTicket
* MySQL Username: root
* MySQL Password: root
* Click “Install Now!”
</p>
<br />

<p>
<img width="628" alt="image" src="https://github.com/user-attachments/assets/f3638e12-a9b6-43a6-b484-5d4782490f8c" />
<img width="628" alt="image" src="https://github.com/user-attachments/assets/dd3bd1be-cb87-4344-a74f-7086542489c3" />

Congratulations, You've installed osTicket.
