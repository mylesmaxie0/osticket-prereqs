<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png"/>
</p>

<h1> How to Install osTicket </h1>
This guide provides simple instructions for installing a help desk ticketing system called osTicket.<br/>

<h2> Files You Need to Download</h2>

- ### [Download Now](https://drive.google.com/drive/u/2/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6) 📁

<h2> Software & Technologies  Used</h2>

- Windows 10 
- Microsoft Azure (Virtual Machines)
- Remote Desktop (RDP)
- Internet Information Services (IIS)

<h2> Prerequisites </h2>

- Create a Virtual Machine in Azure
- Install osTicket v1.15.8
- Install HeidiSQL
- Install MySQL
- Install PHP
- install Microsoft Visual C++ Redistributable
  <h2>Steps</h2>
<h3 align="center">Create Virtual Machine in Azure</h3>
<br />
<p>
<h3 align="center">Start by creating a Resource Group in Azure.</h3>
<br />
</p>
<p>
<img src="https://i.imgur.com/eBi5k2l.png" height="75%" width="100%" />
</p>
<p>
<h3 align="center">Next, create a Windows 10 Virtual Machine (VM) with 2-4 virtual CPUs. Set a username and password of your choice, as this information will be used to remotely access the VM from your main computer. During the VM creation process, let Azure automatically create a new Virtual Network (VNet).</h3>
<br />
</p>
<p>
	<img src="https://i.imgur.com/dEF1c7h.png" height="75%" width="100%" />
</p>
<h3 align="center">Open your Remote Desktop Connection app on your computer and connect to your Virtual Machine that was created in Azure. </h3>
<br />
<p>
	<img src="https://github.com/Joeljjoseph1998/osticket-prereqs/assets/50834280/2e71fd86-4198-47aa-aa1a-d0aed1b8e0eb"/>
	

</p>
<h3 align="center">Next, install and enable IIS (Internet Information Services) in Windows:
Open the Search Bar and type "Control Panel".
Click on "Programs".
Select "Turn Windows features on or off".
Scroll down and check the box for "Internet Information Services (IIS)".
Click OK to apply the changes.</h3>
<br/>
<p>
	<img src="https://i.imgur.com/iB0DDRd.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">After enabling IIS:

Expand "Internet Information Services".
Expand the "World Wide Web Services" section.
Expand the "Application Development Features" tab.
Check the box for "CGI" and click OK.
Enabling CGI is necessary to install the PHP Manager. PHP is a back-end web programming language that allows osTicket to operate via a web browser.</h3>
<br />
<p>
  <img src="https://github.com/Joeljjoseph1998/osticket-prereqs/assets/50834280/a6af9c35-e10c-4d7e-b2c8-30ffbe128f08" height="75%" width="100%"/>
</p>
<br />
<h3 align="center">Install PHP Manager</h3>
<br />
<p>
<h3 align="center">Download the PHP Manager file and agree to the terms and conditions during the installation process. Once completed, the PHP Manager will be successfully installed on your operating system.</h3>
<p>
  <img src="https://i.imgur.com/pmwpPEu.png"height="75%" width="100%"/>
</p>
<br/>
<h3 align="center">Install Rewrite Module</h3>
<br />
<p>
<h3 align="center">Download the Rewrite Module file, agree with all the terms and it should now be installed onto the Computer.</h3>
<p>
  <img src="https://github.com/Joeljjoseph1998/osticket-prereqs/assets/50834280/28cf2dd0-d39e-45f8-a01b-61aec6657228"height="75%" width="100%"/>
</p>
<br/>
<h3 align="center">CREATE DIRECTORY C:\PHP</h3>
<br />
<p>
<h3 align="center"> Open File Explorer, type, "C:\" in the search bar, Right-click and create a new folder called, "PHP". Download php-7.3.8-nts-Win32-VC15-x86.zip from<a href="https://drive.google.com/drive/u/2/folders/1APMfNyfNzcxZC6EzdaNfdZsUwxWYChf6"> Files You Need to Download</a>, Extract it by going to where you download the file, Right-click the PHP 7.3.8 file and press extract to the PHP Folder you just created.
</h3>
<p>
  <img src="https://github.com/Joeljjoseph1998/osticket-prereqs/assets/50834280/18746085-a3cf-4f1f-b0d5-5cd73f969319"height="75%" width="100%"/>
</p>
<br/>
<h3 align="center">VC_REDIST DOWNLOAD</h3>
<br/>
<h3 align="center"> Download and install VC_Redist, Agree with any terms and agreements and finish installing.
</h3>
<p>
  <img src="https://i.imgur.com/Gx8ryBV.png"75%" width="100%"/>
</p>
<br/>
<h3 align="center">DOWNLOAD MySQL </h3>
<h3 align="center"> Download and install MySQL, Agree with any terms and agreements up until you get to the password portion. Here you can create a username and password for the database that you'll be using to store the Ticket Information used in osTicket. 
</h3>
<p>
  <img src="https://i.imgur.com/IVpLg40.png"75%" width="100%"/>
<br/>
  <img src="https://i.imgur.com/zdhWXNx.png" height="75%" width="100%" />
</p>
<br/>
<h3 align="center">Install osTicket v1.15.8</h3>
<br />
<p>
  Download osTicket (download from within lab files: link).
</p>
<p>
	Extract and copy the “upload” folder INTO c:\inetpub\wwwroot:
</p>
	<img src="https://i.imgur.com/0MUJLMU.png" height="75%" width="100%" />
	<img src="https://i.imgur.com/1h9goM8.png" height="75%" width="100%" />
<p>
	Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”:
</p>
<p>
	<img src="https://i.imgur.com/pDikkgq.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Reload IIS (Open IIS, Stop and Start the server)</h3>
<br />
<p>
	Go to sites -> Default -> osTicket:
</p>
<p>
	<img src="https://i.imgur.com/QeWNlG3.png" height="75%" width="100%" />
</p>
<p>
	On the right, click “Browse *:80”:
</p>
<p>
	<img src="https://i.imgur.com/3iXhNbi.png" height="75%" width="100%"/>
</p>
<br />
<br />
<h3 align="center">Enable Extensions in IIS: Note that some extensions are not enabled</h3>
<br />
<p>
	Go back to IIS, sites -> Default -> osTicket.
</p>
<p>
	Double-click PHP Manager:
</p>
<p>
	<img src="https://i.imgur.com/LFKo5Hs.png" height="75%" width="100%" />
</p>
<p>
	Click “Enable or disable an extension”.
</p>
<p>
	Enable: php_imap.dll.
</p>
<p>
	Enable: php_intl.dll.
</p>
<p>
	Enable: php_opcache.dll:
</p>
<p>
	<img src="https://imgur.com/a/nrQo0kz" height="75%" width="100%"/>
</p>
<br />
<br />
<h3 align="center">Refresh the osTicket site in your browser, observe the changes</h3>
<br />
<p>
	<img src="https://i.imgur.com/6iSNd4H.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Rename</h3>
<br />
<p>
	From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php.
</p>
<p>
	To: C:\inetpub\wwwroot\osTicket\include\ost-config.php:
</p>
<p>
	<img src="https://i.imgur.com/TEw71SD.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Assign Permissions: ost-config.php</h3>
<br />
<p>
	Disable inheritance -> Remove All:
</p>
<p>
	<img src="https://i.imgur.com/1QtRWEF.png" height="75%" width="100%" />
</p>
<p>
	New Permissions -> Everyone -> All:
</p>
<p>
	<img src="https://i.imgur.com/YzsMXNX.png" height="75%" width="100%" />
</p>
<p>
	<img src="https://i.imgur.com/k7x9yGR.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Continue Setting up osTicket in the browser (click Continue)</h3>
<br />
<p>
	Name Helpdesk.
</p>
<p>
	Default email (receives email from customers):
</p>
<p>
	<img src="https://i.imgur.com/rvMvlNC.png" height="75%" width="100%" />
	<img src="https://i.imgur.com/YszhIpl.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Download and Install HeidiSQL</h3>
<br />
<p>
	<img src="https://i.imgur.com/AEg0b2P.png" height="75%" width="100%" />
</p>
<p>
	Create a new session, root/Password1.
</p>
<p>
	Connect to the session:
</p>
<p>
	<img src="https://i.imgur.com/9t51ApR.png" height="75%" width="100%" "/>
</p>
<p>
	Create a database called “osTicket”:
</p>
<p>
	<img src="https://i.imgur.com/vXzmQqg.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Continue Setting up osTicket in the browser</h3>
<br />
<p>MySQL Database: osTicket</p>
<p>
	MySQL Username: root
</p>
<p>
	MySQL Password: Password1:
</p>
<p>
	<img src="https://i.imgur.com/akDyber.png" height="75%" width="100%" />
</p>
<p>Click “Install Now!”</p>
<p>Congratulations, hopefully it is installed with no errors!</hp>
<p>
	<img src="https://i.imgur.com/J5omRoE.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Clean up</h3>
<br />
<p>
	Delete: C:\inetpub\wwwroot\osTicket\setup:
</p>
<p>
	<img src="https://i.imgur.com/eg0ZPG3.png" height="75%" width="100%" />
</p>
<p>
	Set Permissions to “Read” only: C:\inetpub\wwwroot\osTicket\include\ost-config.php:
</p>
<p>
	<img src="https://i.imgur.com/n6k46XL.png" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center">Login to the osTicket Admin Panel (http://localhost/osTicket/scp/login.php)</h3>
<br />
<p>
	<img src="https://i.imgur.com/8wvWH0H.jpg" height="75%" width="100%" />
</p>
<br />
<br />
<h3 align="center"> Congrats, You've Finished Installing osTicket.</h3>
