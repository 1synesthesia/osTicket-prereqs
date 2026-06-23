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

- Windows 11 Pro </b> (21H2)

<h2>List of Prerequisites</h2>

- HeidiSQL
- osTicket
- PHP Mananger for IIS: <https://www.iis.net/downloads/community/2018/05/php-manager-150-for-iis-10/>
- Rewrite Module: <https://www.iis.net/downloads/microsoft/url-rewrite>
- PHP Database: <https://downloads.php.net/~windows/releases/archives/>
- mySQL
- VC Redistributable

<h2>Installation Steps</h2>

<p>
<h1>ALWAYS MAKE SURE TO USE MOST UP TO DATE VERSION OF EACH PREREQ</h1>
</p>
<h3>Step 1: Activate IIS</h3>
<p>
<img width="1121" height="630" alt="Screenshot 2026-06-23 010532" src="https://github.com/user-attachments/assets/f42dc5ac-02db-405f-8e9f-d64e63fede14" />
</p>
<p>
Naviagte to Control Panel then select uninstall a program. Once you are there you will want to click 'Turn Windows features on or off'. Then you will want to actiavte Internet Information Services and make sure to expand and navigate to World Wide Web services. Expand the WWWS, find Application Development Features and expand, and then check the box next to CGI (do not forget this step otherwise osTicket will not work). Once you have double checked to make sure everything is the same as the screenshot above you can click ok which will install IIS with CGI.
</p>
<br />

<h3>Step 2: Install PHP Manager for IIS</h3>
<p>
<img width="495" height="406" alt="Screenshot 2026-06-23 011935" src="https://github.com/user-attachments/assets/b2ffc01b-36be-468d-84ed-cf96cb370c95" />
</p>
<p>
Next you will want to install a PHP Manager for IIS. Simply go to the link above in the Prequisites and download. This will be used to register a PHP with IIS and allow you to access all the features necessary for osTicket.
</p>
<br />
<h3>Step 3: Install Microsoft URL Rewrite Extension</h3>
<p>
<img width="364" height="85" alt="image" src="https://github.com/user-attachments/assets/b3f0a181-ccba-4d8a-aa17-98895b9f0037" />
</p>
<p>
Now you will simply download the Rewrite Module necessary for osTicket. Make sure to install the x64 version for whatever language you require (English shown above for this demo).
</p>
<br />

<h3>Step 4: Create a PHP Directory</h3>
<p>
<img width="1121" height="630" alt="Screenshot 2026-06-23 012929" src="https://github.com/user-attachments/assets/7fb4a724-ecde-48b1-a7f3-c67830e3a07b" />
</p>
<p>
The next step will be to simply create a folder on your C: drive named PHP.
</p>
<br />

<h3>Step 5: Install and unzip your PHP Database into your PHP directory</h3>
<p>
<img width="514" height="21" alt="Screenshot 2026-06-23 013724" src="https://github.com/user-attachments/assets/c3d48c50-f55b-4f66-8fd4-5773dd25a593" />
<img width="611" height="449" alt="Screenshot 2026-06-23 014005" src="https://github.com/user-attachments/assets/e0fd6863-c1e0-4065-a71d-2d7f63f74684" />
</p>
<p>

</p>
