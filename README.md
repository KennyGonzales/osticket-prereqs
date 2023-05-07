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
  
We will now connect to the VM with `Remote Desktop Connection`. Use the VM's public IPv4 to connect.
  
<img src="https://i.imgur.com/5luMEbS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>

</p>
<br />

<p>
  
After establishing a connection and accessing the virtual machine, the next step is to install the Web Platform Installer. To do so, we need to locate the `Control Panel` and select **Uninstall a program** from the 'Programs' section.
  
<img src="https://i.imgur.com/B7qxI43.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
<img src="https://i.imgur.com/DplZJ1N.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</p>
<br />


<p>

Once we have accessed the next page, we can proceed to select `Turn Windows features on or off` and then activate the `Internet Information Services` (IIS) from the list of available services. Turn on CGI, which is under **Applications Development Features**

<img src="https://i.imgur.com/WUN7tQ9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/kCmXm10.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</p>
<br />


<p>
        
After applying the changes, we will need to download/install `PHP Manager` & `rewrite module` from the installation files. After downloading those files, create a directory for `PHP`. 

>**Note**: Download the files on Google Drive through the **Windows VM**.
  
<img src="https://i.imgur.com/qoApMMC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</p>
<br />


<p>

From the installation files, download `PHP 7.3.8` and extract the contents into `c:/PHP`. After, download `VC_redist` and `MySQL 5.5.62`.

<img src="https://i.imgur.com/J4jPymw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</p>
<br />

<p>
  
We need to create a root password once ‘MySQL 5.5.62’ is downloaded. **Typical Setup** -> **Launch Configuration Wizard** (after install) -> **Standard Configuration** -> **Create Password**. 

>**Note**: I suggest creating a notepad/notes to write usernames and passwords for this activity.
 
<img src="https://i.imgur.com/dMBP4s9.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</p>
<br />

<p>
  
To register a new PHP version, we first need to access the IIS (Internet Information Services) by typing "IIS" in the Start menu and running it as an administrator. Once we have access, we can then open `PHP Manager` by double-clicking on it and selecting `Register new PHP version`.  
  
<img src="https://i.imgur.com/Onk3tUY.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/hcstAyq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</p>
<br />

<p>
  
After downloading the necessary files, we need to install and extract the osTicket file. Next, we should extract the file and copy the `"upload"` folder to the directory **c:\inetpub\wwwroot**. Then, we should rename the `"upload"` folder to `"osTicket"` within the **c:\inetpub\wwwroot directory**.
  
<img src="https://i.imgur.com/IyTuwts.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<img src="https://i.imgur.com/ie0NaQA.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>  
</p>
<p>
</p>
<br />

<p>
  
Open IIS & restart server. Once finished, go to **sites** -> **default web site** -> **osTicket** ; click on **Browse * :80**
  
<img src="https://i.imgur.com/9W0L8pC.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</p>
<br />

<p>
  
After clicking **Browse * :80**, this selected browser will be presenting the osTicket installer page. Some recommendations will be disabled. 
  
<img src="https://i.imgur.com/14jDUKb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</p>
<br />

<p>
  
In IIS, we will go to **Sites** -> **Default** -> **osTicket**. We will double click `PHP Manager`, and click `enable or disable an extension`. From there, we will enable `php_imap.dll`, `php.intl.dll`, & `php_opcache.dll`. 

<img src="https://i.imgur.com/txv6rSx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>  
<img src="https://i.imgur.com/KiVyWyk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</p>
<br />

<p>
  
After enabling the PHP extensions, refresh the osTicket site.  
  
<img src="https://i.imgur.com/hwTYWm3.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
</p>
<br />

<p>
  
Rename `C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php` -> to `C:\inetpub\wwwroot\osTicket\include\ost-config.php.`

<img src="https://i.imgur.com/61IfDc2.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>  
<img src="https://i.imgur.com/JdQ8M94.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
