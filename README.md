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
- PHP Database
- mySQL
- VC Redistributable

<h2>Installation Steps</h2>

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

</p>
