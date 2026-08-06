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
