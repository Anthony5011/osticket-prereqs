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

- Windows 11</b> (25H2)

<h2>List of Prerequisites</h2>

- Azure Virtual Machine
- osTicket Installation files
- Heidi SQL

<h2>Installation Steps</h2>

<p>First, in Azure, create a resource Group.</p>
<p>
<img width="2438" height="1466" alt="image" src="https://github.com/user-attachments/assets/0a704fd3-b9f9-4fc2-9200-d8cabba7b966"/>
</p>
<br />

<p>
After creating a resource group, you will then create a virtual machine under this resource group. This virtual machine will be an Azure virtual machine with Windows 11, 4 vCPUs. The username and password you create are what will be used to remote into your virtual machine from your physical computer.
</p>
<p>
<img width="1756" height="1334" alt="image" src="https://github.com/user-attachments/assets/a0027a02-9506-452b-8ca9-1cb7e5b3b462" /> 
</p>
<br/>

<p>
Then open up the Remote Desktop App to log into the virtual machine that you created in Azure. For users on Mac, you will need to download the Remote Desktop (Windows) App in the App Store. To log into your virtual machine you will first need to add the device in the Remote Desktop app. To do this, you need the public IP address for your virtual machine which can be found in Azure.
</p>
<p>
<img width="1820" height="490" alt="image" src="https://github.com/user-attachments/assets/4f33bcb6-9978-427c-88a5-aa8a9824abfd" />
<img width="1976" height="1140" alt="image" src="https://github.com/user-attachments/assets/84a77772-44cf-46d7-b7f6-fac7d5e1176b" />
</p>
<br/>

<p>
Now we must install/enable IIS on the Windows computer with CGI including application features and IIS Management Console. This is what allows the computer to be turned into a web server. You do this by going to your search bar > type "Control Panel" > click uninstall a program in "Programs" > click "Turn Windows features on or off" > Scroll down to "Internet Information Services (IIS) > click "World Wide Web Services" > click "Application Development Features" > click CGI. Also, make sure that IIS Management Console is enabled. You can do this by clicking "Web Management Tools" instead of WWW Services.
</p>
<p>
<img width="2872" height="1594" alt="image" src="https://github.com/user-attachments/assets/929a17e2-43e4-457e-9482-be125bdea223" />
</p>
<br/>

<p>
Excellent. Now that you have enabled IIS, you will access a group of files that will provide you with all of the downloadable materials you need to get osTicket running. I have provided a link here: https://drive.usercontent.google.com/download?id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD&export=download&authuser=0
</p>
<p>
<img width="2866" height="1040" alt="image" src="https://github.com/user-attachments/assets/6c2d9070-edc7-4a1f-9dac-21cfb4a4d2e9" />
<img width="2632" height="1106" alt="image" src="https://github.com/user-attachments/assets/76095668-e1ca-42d7-8355-4a6c40f76faa" />
</p>
<br />

<p>
From the "osTicket-Installation-Files" folder, install PHP Manager for IIS. 
</p>
<p>
<img width="1002" height="824" alt="image" src="https://github.com/user-attachments/assets/75149517-5d7a-45a6-9cd4-b204f7e0be02" />
</p>
<br/>

<p>
From the same folder, install the Rewrite Module.
<p>
<p>
<img width="990" height="782" alt="image" src="https://github.com/user-attachments/assets/513f35df-eb51-40ec-8c0b-5ae2cfbda6a4" />
</p>
<br/>

<p>
Next up, you need to create the directory C:\PHP. Open File Explorer, type, "C:\" in the search bar, Right-click and create a new folder called, "PHP". Unzip the php-7.3.8-nts-Win32-VC15-x86.zip from the "osTicket-Installation-Files" folder into the PHP folder you just created. To do this, you need to right click the php 7.3.8 file and click "Extract all" > browse to the C\PHP folder > select the folder > click extract.
</p>
<p>
<img width="1224" height="908" alt="image" src="https://github.com/user-attachments/assets/d6c85130-813e-49a6-81cf-ae02e46667f3" />
</p>
<br/>

<p>
From the "osTicket-Installation-Files" folder, install VC Redist.
</p>
<p>
<img width="960" height="600" alt="image" src="https://github.com/user-attachments/assets/28f4f827-f5ed-450c-8c02-80ea3590bc57" />
</p>
<br/>

<p>
From the same folder, instal MySQL database. The typical setup for it is -> click Launch Configuration Wizard -> Standard Configuration -> create username and password.
</p>
<p>
<img width="992" height="778" alt="image" src="https://github.com/user-attachments/assets/a30c7514-dc49-4eb5-ae75-6c7f952147e6" />
</p>

<p>
Open IIS as an Admin then Register PHP from within IIS (PHP Manager > C:\PHP\php-cgi.exe)
</p>
<p>
<img width="2126" height="1222" alt="image" src="https://github.com/user-attachments/assets/113458b3-5667-47bd-be4b-d438881268f6" />
</p>
<br/>

<p>
From the “osTicket-Installation-Files” folder, unzip “osTicket-v1.15.8.zip” by extracting all and copy the “upload” folder into “c:\inetpub\wwwroot”. Within “c:\inetpub\wwwroot”, rename “upload” to “osTicket”
</p>
<p>
<img width="2234" height="1122" alt="image" src="https://github.com/user-attachments/assets/10b77aec-e47e-47dc-a420-8c3a8a9b1ac2" />
<img width="2242" height="1182" alt="image" src="https://github.com/user-attachments/assets/c7e62877-59a7-4488-a78e-e2e0d9b4534b" />
<img width="2242" height="1182" alt="image" src="https://github.com/user-attachments/assets/1fe2c28b-8306-4b09-9550-aa744e9d381c" />
</p>
<br/>

<p>
To see how the website currently looks, go to sites > Default > osTicket. On the right, click "Browse *:80" 
</p>
<p>
<img width="2124" height="1214" alt="image" src="https://github.com/user-attachments/assets/ed4c2db1-4996-4f56-86b9-1b7f5fd09ebd" />
<p>Note that some extensions are not enabled
<img width="2878" height="1620" alt="image" src="https://github.com/user-attachments/assets/5510fb37-a818-41ad-b77e-793f8f1d693b" />
</p>
</p>
<br/>

<p>
To enable some of the extensions needed for functionality of osTicket, go back to IIS > click sites > default > osTicket > double-click PHP Manager > click "Enable or disable an extension". Enable: php_imap.dll, php_intl.dll, php_opcache.dll. Then refresh the osTicket site in your browser and observe the changes.
</p>
<p>
<img width="2126" height="1218" alt="image" src="https://github.com/user-attachments/assets/5197947f-9043-4b12-a862-e789e2f2c88c" />
<img width="2122" height="1216" alt="image" src="https://github.com/user-attachments/assets/968307ee-a9dc-4df1-bfc6-16c35ce46243" />
<img width="2860" height="1614" alt="image" src="https://github.com/user-attachments/assets/875ac226-26e6-4c44-bcc1-212ef93d9fd2" />
</p>
<br/>

<p>
Rename ost-config.php. To do this, go to the C drive > click inetpub > click wwwroot > click osTicket > click "include" folder. Change C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php to C:\inetpub\wwwroot\osTicket\include\ost-config.php
</p>
<p>
<img width="2244" height="1182" alt="image" src="https://github.com/user-attachments/assets/37312335-f625-460e-8a1f-b30341396475" />
</p>
<br/>

<p>
Assign permissions to ost-config.php. Right click on the file > click properties > click security > click Advanced > click disable inheritance > click remove all > click add new permissions > select a principal > click everyone > all boxes checked > click apply > click ok
</p>
<p>
<img width="1532" height="1044" alt="image" src="https://github.com/user-attachments/assets/af6ff67f-3bfc-4111-96e0-7e323d674303" />
</p>
<br/>

<p>
Now click continue to proceed with setting up osTicket in the browser. First name the help desk, then give a default email that receives email from customers, and then provide an admin user.
</p>
<p>
<img width="2558" height="1608" alt="image" src="https://github.com/user-attachments/assets/b8045114-8f81-46e4-98d4-48294b352426" />
</p>
<br/>

<p>
From the "osTicket-Installation-Files" folder, install HeidiSQL. Then open Heidi SQL (which is an application that allows us to make a connection to our database) > create a new session with username/password > connect to the session > create a database called "osTicket"
</p>
<p>
<img width="1368" height="966" alt="image" src="https://github.com/user-attachments/assets/5a86232e-9fc6-4c7f-8d64-4cbf567b1a03" />
<img width="1956" height="1032" alt="image" src="https://github.com/user-attachments/assets/382f8228-ca6f-4b4a-aed5-318493b5f8e4" />
</p>
<br/>

<p>
Continue setting up osTicket in the browser. After submitting info for MySQL Database, username, and password, click "Install Now!"
</p>
<p>
<img width="1912" height="1550" alt="image" src="https://github.com/user-attachments/assets/c71827cf-2eba-4a5b-bd8c-45a6d8c14c5f" />
</p>
<br/>

<p>
Confirm osTicket can be reached by users on LocalHost.
</p>
<br/>

<p>
Test link for agents and end-users:
</p>
<p>
Agents URL: http://localhost/osTicket/scp/login.php
</p>
<p>End Users URL: http://localhost/osTicket/
</p>
<br/>
<p>
Clean up files that pose a security risk
</p>
<p>
Delete: C:\inetpub\wwwroot\osTicket\setup.
</p>
<p>
Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php.
</p>
