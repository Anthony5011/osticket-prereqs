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

</p>
<br />

<p>
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
Lorem ipsum dolor sit amet, consectetur adipiscing elit, sed do eiusmod tempor incididunt ut labore et dolore magna aliqua. Ut enim ad minim veniam, quis nostrud exercitation ullamco laboris nisi ut aliquip ex ea commodo consequat. Duis aute irure dolor in reprehenderit in voluptate velit esse cillum dolore eu fugiat nulla pariatur.
</p>
<br />
