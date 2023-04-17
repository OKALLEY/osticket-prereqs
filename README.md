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
</h2>https://drive.google.com/drive/folders/1HhS1aa-H8trQa0IPt1hn0Q7-X_vTCk5n?usp=share_link 
<h2>Installation Stages</h2>

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
<li>Choose the same Region as your Resource Group</li>
<li>Generate a Windows 10 computer under image</li>
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
Stage 3:

</p>
<br />
