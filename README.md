<p align="center">
<img src="https://imgur.com/Owq9lOV.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
~This tutorial covers the necessary prerequisites and installation process for osTicket - an open-source help desk ticketing system.~<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Install / Enable IIS (Internet Information Services)
- Install PHP Manager for IIS
- Install Rewrite Module
- Download and Unzip PHP
- Install C++ Redistributable 
- Install MySQL
- Configure Permissions
<h2>Links:
osTicket Installation Files
</h2>https://drive.google.com/drive/folders/1HhS1aa-H8trQa0IPt1hn0Q7-X_vTCk5n?usp=share_link<h2>
Virtual Machine Creation</h2>

<p>
Stage 1: Create a Resource Group in Azure
<img src="https://imgur.com/nNY8hrj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/> 
<li>Give your Resource Group a name</li>
<li>Choose a Region</li> 
<li> Click the "Review + Create" tab</li>  
NOTE: Use the same Region when creating your Virtual machines
<img src="https://imgur.com/TuybLQq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<li>Click the "Create" tab (bottom left corner)</li>  
<img src="https://imgur.com/OLxYtk5.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<p>
Stage 2: Create a Virtual Machine in Azure
<ul>
<li>Create a Windows 10 Virtual Machine (VM) with 2-4 Virtual CPU</li>
NOTE: When creating the VM, allow it to create a new Virtual Network (Vnet)

</p>
<img src="https://imgur.com/F5j2Ukt.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<li>Assign the resource group you created</li>
<li>Name your virtual machine</li>
<li>Select your Region</li>
<li>Generate a Windows 10 computer under Image</li>
<img src="https://imgur.com/ay9MfRj.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<li>Choose the size of your virtual machine (2 vcpus)</li>
<li>Choose a user name and password</li>
<img src="https://imgur.com/3Cjhjwb.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<li>Check the box to confirm Licensing</li>
<li>Click the tab "Next : Disks >" then "Next : Networking >"</li>
</p>
<img src="https://imgur.com/JEvqBAi.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

<p>
<img src="https://imgur.com/9VdXzrS.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<li>Here you can take note of your new Virtual Network, private IP followed by your public IP.</li>
<li>Click the "Review + Create" tab  and once validation is complete click "Create".</li>
</p>
<br />

<p>
<img src="https://imgur.com/5tbmena.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
<h2>Installation</h2> 
<li>In Azure under Virtual Machines find and click your virtual machine. Locate its Public IP address. Click to copy it.</li>
<li>In Windows click start and type: Remote Desktop Connection. (Mac users install Microsoft Remote Desktop)</li>
<img src="https://imgur.com/PneTRfI.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<li>Paste the IP address and click the Connect tab</li>
<li>Enter your user name and password you made when you created your virtual machine</li>
<img src="https://imgur.com/kXcqJgR.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<li>Click "Yes"</li>
<img src="https://imgur.com/mBmdCxB.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<br />
<li>Right click the start menu and click "Run"</li>
<li>Type "control" for Control Panel and press enter</li>
<img src="https://imgur.com/lM0F2of.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
</p>
<li>CLick Programs and select "Turn Windows Features On or Off"</li>
<img src="https://imgur.com/JEaj2Sw.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/IEIkrMR.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
</p>
<li>Turn on "Internet Information Services (IIS) and then click the box to the left to expand</li>
<li>Expand "World Wide Web Services"</li>
<li>Expand "Application Development Features"</li>
<li>Check the box for "CGI" and press OK and once changes have been applied click Close</li>
<img src="https://imgur.com/vEaf4nV.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<li>To confirm your web server is working, open a browser and type 127.0.0.1</li>
<li>This should load the default ISS website:</li>
<img src="https://imgur.com/850Le0m.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<br />
<h2>For this next stage refer back to Links: osTicket Installation Files:</h2>
https://drive.google.com/drive/folders/1HhS1aa-H8trQa0IPt1hn0Q7-X_vTCk5n?usp=share_link</h2> 

<p>
<li> Install PHP Manager for IIS</li> 
<img src="https://imgur.com/wksFCHu.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<img src="https://imgur.com/kNCt1xp.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
  
<li>Open the Downloads folder and double click and install it (Next; I Agree; Next; Close).
<p>
<p>  
<li>Download and install the URL Rewrite Module</li>
<img src="https://imgur.com/eU1TVw8.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>
  
<br />
<p>
<p>
<li>Create the directory C:\PHP</li>
<li>To do this go to "This PC" and under Devices and drivers choose Windows (C:)</li>
<img src="https://imgur.com/mLo3568.png" height="40%" width="40%" alt="Disk Sanitization Steps"/>  
<li>Right click and create and name a Folder "PHP"</li>  

<li> Next refer back to osTicket Installation Files and download 
<a href="https://drive.google.com/file/d/1LmwEE6wNKhfijJ1pyQj_cPVh8rYFzIpa/view?usp=share_link" target="_blank">PHP Manager for IIS</a>
<li>In the downloads folder right click and Extract All...</li>
<img src="https://imgur.com/z9XMFEI.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<li>Extract to the PHP folder you created: Browse; This PC; Windows (C:); then click on the PHP folder
<img src="https://imgur.com/1Uu58GZ.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<li>Click "Extract"  </li>
  <p>
    
<li> Download and Install VC_redist.x86.exe (C++ Redistributable)</li>
<img src="https://imgur.com/EgQzNPu.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>
<li>Go back to Downloads and click on it to install: I agree; Install; Close</li>    
<img src="https://imgur.com/W8OjLpp.png" height="50%" width="50%" alt="Disk Sanitization Steps"/>

<p>
<li>Download and install MySQL Server</li>   
<img src="https://imgur.com/atZnobW.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
<li>Next</li>  
<img src="https://imgur.com/Zg4AkCm.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
<li>I accept...; Next</li>  
<img src="https://imgur.com/Zg4AkCm.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
<li>Choose Typical and Install</li>  
<img src="https://imgur.com/AUyOpZB.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
<li>The box for "Launch the MySQL Instance Configuration Wizard" should be checked. Click Finish</li>
<img src="https://imgur.com/Eak8nJh.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
<li>Click Next then choose "Standard Configuration" and click Next</li> 
<img src="https://imgur.com/byg5A7Q.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
<li>Check "Install As Windows Service" and click Next</li>

<p>
<li>Note that in MySQL your User Name is "root"</li>
<li>Assign a password and click Next then click Execute</li>
<img src="https://imgur.com/lElrevv.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
<li>Execute and allow it to finish configuring MySQL Server</li>  
<img src="https://imgur.com/lwunntS.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>
<Li>and click Finish</li>
<img src="https://imgur.com/5gx7izp.png" height="60%" width="60%" alt="Disk Sanitization Steps"/>  
  
<p>
<h2>Configuration</h2>   
  
