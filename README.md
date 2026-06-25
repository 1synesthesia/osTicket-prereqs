<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>What is osTicket and why use it?</h1>
<p>The main use for osTicket is as a ticketing system for IT Help Desk scenarios. It allows for easy communication between users, agents, and admins about all sorts of help desk scenarios. The best reason to use osTicket is that it is a practically fully customizable software which can be configured to be used in whatever way best fits your companies needs. It is also an open source platform allowing you to save costs and allows you to adjust the coding as you see fit.
</p>
<br />

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />

<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machines/Compute)
- Remote Desktop
- Internet Information Services (IIS)
- osTicket

<h2>Operating Systems Used </h2>

- Windows 11 Pro </b>

<h2>List of Prerequisites</h2>

- <a href="https://www.heidisql.com/download.php">HeidiSQL</a>
- <a href="https://osticket.com/download/">osTicket Installer</a>
- <a href="https://github.com/RonaldCarter/PHPManager/releases)/">PHP Manager for IIS</a>
- <a href="https://www.iis.net/downloads/microsoft/url-rewrite">C++ Rewrite Module</a>
- <a href="https://downloads.php.net/~windows/releases/archives/">PHP Scripting Language</a>
- <a href="https://dev.mysql.com/downloads/mysql/">mySQL Database</a>
- <a href="https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-170&viewFallbackFrom=msvc-170%2F">VC Redistributable</a>

<h2>Configuring your Azure VM</h2>

<p>
<img width="789" height="1305" alt="Screenshot 2026-06-24 232049" src="https://github.com/user-attachments/assets/525a0196-63e4-4929-8593-cf30d0f21882" />
</p>
<p>
* Your first step to setting up your Azure VM is to create a resource group to put it in. The only important step here is to name it!
</p>


<h2>Installation Steps</h2>

<p>
<h1>ALWAYS MAKE SURE TO USE THE MOST UP TO DATE VERSION OF EACH PREREQ</h1>
</p>

<h3>Step 1: Activate IIS (Internet Information Services)</h3>
<p>
<img width="1121" height="630" alt="Screenshot 2026-06-23 010532" src="https://github.com/user-attachments/assets/f42dc5ac-02db-405f-8e9f-d64e63fede14" />
</p>
<p>
• Navigate to Control Panel and then select uninstall a program. Once you are there you will want to click 'Turn Windows features on or off'. Then you will want to activate Internet Information Services and make sure to expand and navigate to World Wide Web services. Expand the WWWS, find Application Development Features and expand, and then check the box next to CGI (do not forget this step otherwise osTicket will not work). 
  
• Once you have double checked to make sure everything is the same as the screenshot above you can click 'ok' which will install IIS with CGI.
</p>
<br />

<h3>Step 2: Install PHP Manager for IIS</h3>
<p>
<img width="495" height="406" alt="Screenshot 2026-06-23 011935" src="https://github.com/user-attachments/assets/b2ffc01b-36be-468d-84ed-cf96cb370c95" />
</p>
<p>
• Next you will want to install a PHP Manager for IIS. Simply go to the link above in the Prequisites and download.
  
• This will be used to register a PHP with IIS and allow you to access all the features necessary for osTicket.
</p>
<br />

<h3>Step 3: Install Microsoft URL Rewrite Extension</h3>
<p>
<img width="364" height="85" alt="image" src="https://github.com/user-attachments/assets/b3f0a181-ccba-4d8a-aa17-98895b9f0037" />
</p>
<p>
• Now you will simply download the Rewrite Module necessary for osTicket. 
  
• Make sure to install the x64 version for whatever language you require (English shown above for this tutorial).
</p>
<br />

<h3>Step 4: Create a PHP Directory</h3>
<p>
<img width="1121" height="630" alt="Screenshot 2026-06-23 012929" src="https://github.com/user-attachments/assets/7fb4a724-ecde-48b1-a7f3-c67830e3a07b" />
</p>
<p>
• The next step will be to simply create a folder on your C: drive named PHP.
</p>
<br />

<h3>Step 5: Install and unzip your PHP scripting language into your PHP directory</h3>
<p>
<img width="259" height="30" alt="Screenshot 2026-06-23 223704" src="https://github.com/user-attachments/assets/1cb6242d-5ed3-45dc-8ffc-f5fa7544fcd5" />
<img width="611" height="449" alt="Screenshot 2026-06-23 014005" src="https://github.com/user-attachments/assets/e0fd6863-c1e0-4065-a71d-2d7f63f74684" />
</p>
<p>
• Now that you have a directory for your PHP; navigate to the most up to date version of the PHP using the link in the prereqs. 
  
• Once you have downloaded the zip file you will want to extract all files into your PHP directory on your C: drive.
</p>
<br />

<h3>Step 6: Install the C++ Redistributable</h3>
<p>
<img width="686" height="140" alt="Screenshot 2026-06-23 014901" src="https://github.com/user-attachments/assets/411e67b7-e6f6-4175-8c4a-c23f23bfe0e0" />
<img width="477" height="297" alt="Screenshot 2026-06-23 015033" src="https://github.com/user-attachments/assets/aa55091c-d503-42e3-aacf-d8b0dcc1fc9c" />
</p>
<p>
• Navigate to the exact link shown in the screenshot and download. 
  
• Once you have downloaded simply install the redistributable.
</p>
<br />

<h3>Step 7: Install mySQL </h3>
<p>
<img width="955" height="355" alt="Screenshot 2026-06-24 003003" src="https://github.com/user-attachments/assets/5d32cea0-47ed-4990-8bee-724b0193378b" />
<img width="490" height="386" alt="Screenshot 2026-06-23 015607" src="https://github.com/user-attachments/assets/1a310267-8f88-4e26-a89f-e8c71a56ffc6" />
</p>
<p>
• Now you will download the latest version of mySQL installer (make sure it is the MSI installer as shown above). The first step in the installation process will be to decide what type of installation setup you would like to use; for the purposes of this tutorial you will use Typical setup.
  
• Once the setup is done you will be taken to the configuration wizard; you will then decide how you would like to configure your mySQL depending on your specific needs. In this case we haven't changed anything; after you have set a user and password for mySQL you can execute the config wizard.
</p>
<br />

<h3>Step 8: Register PHP within IIS</h3>
<p>
<img width="826" height="863" alt="Screenshot 2026-06-23 020333" src="https://github.com/user-attachments/assets/03cb3a3b-dc1f-4a5b-b03e-8f7c71ce3903" />
<img width="1178" height="706" alt="Screenshot 2026-06-23 020456" src="https://github.com/user-attachments/assets/2c17f223-3a34-439d-9855-cba34a807e14" />
</p>
<p>
• Open Internet Information Services Manager as administrator. Once open navigate to PHP Manager and click 'register new PHP version'. The .exe file necessary will be found within your PHP directory on your C: drive. 
  
• After you have registered the PHP simply restart the IIS server at the home page under Actions>Manage Server. 
</p>
<br />

<h3>Step 9: Download and install osTicket</h3>
<p>
<img width="1470" height="668" alt="Screenshot 2026-06-23 021510" src="https://github.com/user-attachments/assets/46a88a01-2392-45f0-87ab-a1b2d1b61619" />
<img width="1147" height="656" alt="Screenshot 2026-06-23 021718" src="https://github.com/user-attachments/assets/c48ac33c-30d8-46d5-a698-0afe692a6d1e" />
<img width="1116" height="632" alt="Screenshot 2026-06-23 021851" src="https://github.com/user-attachments/assets/59430960-1710-4b2f-9032-5fc01f6c678c" />
<img width="1902" height="1010" alt="Screenshot 2026-06-23 022242" src="https://github.com/user-attachments/assets/fc7ec74c-23f5-4674-ae92-ed807e391375" />
</p>
<p>
• Using the link in the prereqs download osTicket by following the steps on the website specific to your installation type. 

• Once downloaded unzip the file onto your computer and copy the upload folder into C: \inetpup\wwwroot. 
  
• After you have copied the folder into wwwroot you must rename it exactly osTicket otherwise osTicket will not work. 

• Now that you have successfully changed the name you can restart the IIS server once again; if done correctly it should look like the last screenshot above.
</p>
<br />

<h3>Step 10: Ensure osTicket Extensions are enabled</h3>
<p>
<img width="1900" height="279" alt="Screenshot 2026-06-23 231345" src="https://github.com/user-attachments/assets/ab92be78-0410-46f0-b4a7-4b5ffb726951" />
<img width="1466" height="368" alt="Screenshot 2026-06-23 231120" src="https://github.com/user-attachments/assets/e107dd2a-35fc-409d-bfa6-092c5c414a77" />
<img width="233" height="15" alt="Screenshot 2026-06-23 230810" src="https://github.com/user-attachments/assets/eb70b327-521d-4626-832d-5f02fb413c1c" />
<img width="818" height="779" alt="Screenshot 2026-06-23 231219" src="https://github.com/user-attachments/assets/acfc7f1f-0f13-4b46-aae7-ee0f00a34ce2" />
</p>
<p>
¥ Now that you have installed osTicket navigate to your new osTicket folder under Sites/Default Web Site. Click on the osTicket folder and click Browse *:80 (http) which should open your osTicket installer. 
  
• You will now need to enable some extensions for osTicket to run smoothly. To enable the extensions go to the PHP Manager on your osTicket folder's home screen; find 'Enable or disable an extension' and enable php_intl.dll, php_imap.dll, and php_opcache.dll (if you are using a newer version of PHP you will need to manually download the <a href="https://pecl.php.net/package/imap/1.0.3/windows">imap extension</a> and place it in your PHP's ext folder,once you are done with that you need to open your php.ini file, find the extensions section, and add ;extension=php_imap.dll; you will also need to ensure that opcache is enabled on newer versions so in that same file find opcache and make sure its value is 1). 

• Once these are enabled restart your server once again and check the installer to make sure it looks like the screenshot above.
</p>
<br />

<h3>Step 11: Enabling osTicket Configuration</h3>
<p>
<img width="1121" height="634" alt="Screenshot 2026-06-23 234710" src="https://github.com/user-attachments/assets/31b376d4-5383-4d3d-8608-6cec5e2629b4" />
<img width="765" height="515" alt="Screenshot 2026-06-23 234928" src="https://github.com/user-attachments/assets/e22720df-46f4-47f4-a378-2a57669563bd" />
</p>
<p>
• Before you can do anything to install osTicket you must change the ost-sampleconfig filename to ost-config and give full permissions to osTicket to make changes.
</p>
<br />

<h3>Step 12: Install HeidiSQL and setup osTicket Database</h3>
<p>
<img width="685" height="481" alt="Screenshot 2026-06-23 235439" src="https://github.com/user-attachments/assets/1d0663be-5d9a-45be-acd2-19fc1f8e4d2d" />
<img width="860" height="458" alt="Screenshot 2026-06-23 235752" src="https://github.com/user-attachments/assets/2cbcb24b-eabd-4d13-88e3-a0e4ce669ef9" />
<img width="820" height="1199" alt="Screenshot 2026-06-23 235826" src="https://github.com/user-attachments/assets/14533e70-2e7c-4d54-88bb-4b356416062b" />
</p>
<p>
• Now that you are on the basic installation page you can fill out the system settings and setup an admin user.
  
• You will now need to setup the mySQL database using HeidiSQL which can be downloaded from the prereqs. 

• Once it is downloaded you will start a new session and sign into the mySQL database with the user and password you setup beforehand. 

• Once connected right click on the database and select create new/database. The database MUST be named osTicket otherwise the installation will not work.

• After the database is setup fill out the database settings section of the installer and click install now. 

• If done correctly you will be sent to a screen that confirms your install and asks you to change the ost.config file to write only permissions; you must do this for osTicket to function securely. Another important security step is to delete the setup folder in your osTicket folder. 
</p>
<br />

<h3>Step 12: Congratulations you have installed osTicket</h3>
<p>
<img width="2158" height="1270" alt="Screenshot 2026-06-24 000816" src="https://github.com/user-attachments/assets/885fd762-0b9a-4237-a209-80d4d32e1a2e" />
<img width="2177" height="1285" alt="Screenshot 2026-06-24 000846" src="https://github.com/user-attachments/assets/37daf3f7-6cdf-4da6-9f71-006158bc74b0" />
</p>
<p>
• Congratulations! You have now succesfully setup and installed an osTicket system.
  
• You can now log into the admin account you setup and start configuring your ticketing system!
</p>
<br />


