<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Video Demonstration</h2>

- ### [YouTube: How To Install osTicket with Prerequisites](https://www.youtube.com)

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Enable "IIS" Internet Information Services
- Install Web Platform Installer
- Install MyCQL + Setup username/password
- Install C++ Redistributable
- Configure Permissions + Install osTicket

<h2>Installation Steps</h2>

<img width="375" alt="image" src="https://github.com/jckjr21/osticket-prereqs/assets/142818746/ff4a03a0-446e-4ff6-8613-ea69631975af">


<p>
</p>
<p>
Install / Enable IIS in Windows with CGI
	
- World Wide Web Services -> Application Development Features ->
-  [X] CGI
- [X] Common HTTP Features

AND IIS Management Console

- Internet Information Services -> Web Management Tools -> IIS Management Console
- [X] IIS Management Console
<img width="242" alt="image" src="https://github.com/jckjr21/osticket-prereqs/assets/142818746/51b650a1-582d-4d26-a448-6002068b3e2e">




  
</p>
<br />

<p>
<img width="361" alt="image" src="https://github.com/jckjr21/osticket-prereqs/assets/142818746/07f57816-9e43-4201-9cf2-e47d61f021b7">

</p>

Download and Install MySQL 5.5.62 (mysql-5.5.62-win32.msi)

- Typical Setup ->
  
- Launch Configuration Wizard (after install) ->

- Standard Configuration ->
  
- Password1

  <img width="361" alt="image" src="https://github.com/jckjr21/osticket-prereqs/assets/142818746/a876395e-d3b8-4bb2-bd11-233f59502f78">


<p>

<br />

<p>
<img width="362" alt="image" src="https://github.com/jckjr21/osticket-prereqs/assets/142818746/fb1f530c-6516-4863-a188-bf9d549f8bda">

</p>
<p>
Install osTicket v1.15.8
	
- Download osTicket from the Installation Files Folder

- Extract and copy “upload” folder to c:\inetpub\wwwroot
Within c:\inetpub\wwwroot, Rename “upload” to “osTicket”


Reload IIS (Open IIS, Stop and Start the server)


- Go to sites -> Default -> osTicket
On the right, click “Browse *:80”
(Note that some extensions are not enabled)


- Go back to IIS, sites -> Default -> osTicket


- Double-click PHP Manager

  
- Click “Enable or disable an extension”


- Enable: php_imap.dll

- Enable: php_intl.dll

- Enable: php_opcache.dll

- Refresh the osTicket site in your browse, observe the changes

Rename: ost-config.php

- From: C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php
  
- To: C:\inetpub\wwwroot\osTicket\include\ost-config.php

Assign Permissions: ost-config.php


- Disable inheritance -> Remove All


- New Permissions -> Everyone -> All

<img width="361" alt="image" src="https://github.com/jckjr21/osticket-prereqs/assets/142818746/4bf7c715-0e3b-4e87-8eb4-ccd9bf04a91e">


</p>
<br />
