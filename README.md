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

- Connect to Virtual Machine w/ Remote Desktop
- Install / Enable IIS in Windows 
- Install Web Platform Installer
- Install osTicket v1.15.8
- Download & Install HeidiSQL
- Created database for osTicket
- Change File Permissions

<h2>Installation Steps</h2>

>**Note**: Before we start this tutorial, we will use these files to install osTicket & some of the dependencies. 

Open here for the files: [osTicket prerequisite and installation files](https://drive.google.com/drive/u/0/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6)

To begin this tutorial, we will need to set up a virtual machine in Microsoft Azure. You can choose any name for the VM that you prefer. The virtual machine should be configured with Windows 10 as its operating system and have 2-4 vCPUs to ensure optimal performance.

<br>
<p>
  
  
<img src="https://i.imgur.com/EgaN4Z7.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</p>
<br />

<p>
  
We will now connect to the VM with 'Remote Desktop Connection'. Use the VM's public IPv4 to connect.
  
<img src="https://i.imgur.com/5luMEbS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
  
After establishing a connection and accessing the virtual machine, the next step is to install the Web Platform Installer. To do so, we need to locate the 'Control Panel' and select **Uninstall a program** from the 'Programs' section.
  
<img src="https://i.imgur.com/pT7DTPU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</p>
<br />


<p>

Once we have accessed the next page, we can proceed to select "Turn Windows features on or off" and then activate the "Internet Information Services" (IIS) from the list of available services.

<img src="https://i.imgur.com/WUN7tQ9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</p>
<br />


<p>
  
Write here   
  
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</p>
<br />


<p>
  
Write here 
  
<img src="https://i.imgur.com/DJmEXEB.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</p>
<br />
