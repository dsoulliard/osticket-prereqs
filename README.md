<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket Installation</h1>
This tutorial outlines the installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10</b> (21H2)

<h2>Installation Steps</h2>

<p>
<img src="https://i.imgur.com/Pz6MvH0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  In control panel, naviagate to programs and features and select "Turn Windows features on or off".
  Enable "Internet Information Services" folder and expand it, then expand "World Wide Web Services", expand 
  "Application Data Features", and enable CGI. Enable all inside of "Common HTTP Features".
</p>
<br />

<p>
<img src="https://i.imgur.com/rZGLJ9G.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  Download and install IIS URL Rewrite Module 2.
</p>
<br />

<p>
<img src="https://i.imgur.com/5ICrEmw.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  Create a new folder on your local hard drive and call it PHP, download and extract PHP to your new folder.
</p>
<br />

<p>
<img src="https://i.imgur.com/nZIKgGu.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  Search for Internet Information Services in your windows search bar, and run the application as an admin.
  Double click on PHP Manager and click on "Register new PHP version", set the destination for the registry, in your   PHP folder select PHP-cgi.exe and restart ISS.

</p>
<br />

<p>
<img src="https://i.imgur.com/13B4hud.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  Download and install MySQL Server and launch it, select Standard Configuration and set your Root Password.
</p>
<br />

<p>
<img src="https://i.imgur.com/8V4Cqoo.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  Download and install osTicket v1.15.8. Inside of the osTicket folder, extract and copy the upload folder into
  "c:\inetpub\wwwroot" and rename the upload folder to "osTicket".
</p>
<br />

<p>
<img src="https://i.imgur.com/UYcxBdU.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  In ISS, open PHP Manager and select "Enable or disable and extension" and enable "php_imap.dll"
  "php_intl.dll" and "php_opcache.dll". After enabling the extensions head to C:\inetpub\wwwroot\osTicket\include
  and change "ost-sampleconfig.php" to "ost-config". Assign permissions for "ost-config" disable inheritance and       remove all permissions and add the principle "Everyone" and give it Full control.
</p>
<br />

<p>
<img src="https://i.imgur.com/SFTFQnq.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  Download and install HeidiSQL, in HeidiSQL create a new connection, set the username and password to the ones     
  chosen in MySQL and open. Create a new database and name it osTicket.
</p>
<br />

<p>
<img src="https://i.imgur.com/YXlOtv0.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
<p>
  Inside of ISS open sites, Default Web Site, then osTicket and select "Browse *.80", this should now take you to the osTicket setup. Click continue and fill out the information with whatever you would like, as long as everything in the MySQL reflects what was put in there. After osTicket is installed, reset permissions in "ost-config" to read only.
</p>
<br />
