<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

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

- HeidiSQL
- osTicket: <https://osticket.com/download/>
- PHP Mananger for IIS: <https://github.com/RonaldCarter/PHPManager/releases)/>
- Rewrite Module: <https://www.iis.net/downloads/microsoft/url-rewrite>
- PHP Database: <https://downloads.php.net/~windows/releases/archives/>
- mySQL: <https://dev.mysql.com/downloads/mysql/>
- VC Redistributable: <https://learn.microsoft.com/en-us/cpp/windows/latest-supported-vc-redist?view=msvc-170>

<h2>Installation Steps</h2>

<p>
<h1>ALWAYS MAKE SURE TO USE THE MOST UP TO DATE VERSION OF EACH PREREQ</h1>
</p>
<h3>Step 1: Activate IIS (Internet Information Services)</h3>
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

<h3>Step 5: Install and unzip your PHP scripting language into your PHP directory</h3>
<p>
<img width="518" height="15" alt="Screenshot 2026-06-23 014342" src="https://github.com/user-attachments/assets/c79501dc-62d8-426d-9dad-8aa7771ab4b4" />
<img width="611" height="449" alt="Screenshot 2026-06-23 014005" src="https://github.com/user-attachments/assets/e0fd6863-c1e0-4065-a71d-2d7f63f74684" />
</p>
<p>
Now that you have a directory for your PHP; navigate to the most up to date version of the PHP using the link in the prereqs (x64 for this demo). Once you have downloaded the zip file you will want to extract all files into your PHP directory on your C: drive.
</p>
<br />

<h3>Step 6: Install the C++ Redistributable</h3>
<p>
<img width="686" height="140" alt="Screenshot 2026-06-23 014901" src="https://github.com/user-attachments/assets/411e67b7-e6f6-4175-8c4a-c23f23bfe0e0" />
<img width="477" height="297" alt="Screenshot 2026-06-23 015033" src="https://github.com/user-attachments/assets/aa55091c-d503-42e3-aacf-d8b0dcc1fc9c" />
</p>
<p>
Navigate to the exact link shown in the screenshot and download. Once you have downloaded simply install the redistributable.
</p>
<br />

<h3>Step 7: Install mySQL </h3>
<p>
<img width="1021" height="764" alt="Screenshot 2026-06-23 015536" src="https://github.com/user-attachments/assets/7f7b0a36-b800-4468-b640-334545a59cc5" />
<img width="490" height="386" alt="Screenshot 2026-06-23 015607" src="https://github.com/user-attachments/assets/1a310267-8f88-4e26-a89f-e8c71a56ffc6" />
<img width="495" height="373" alt="Screenshot 2026-06-23 015640" src="https://github.com/user-attachments/assets/e3bdc97a-bb92-4264-838f-0e5dfcf4d5d5" />
</p>
<p>
Now you will download the latest version of mySQL installer. The first step in the installation process will be to decide what type of installation setup you would like to use; for the purposes of this demo you will use Typical setup. Once the setup is done you will be taken to the configuration wizard; you will then decide what type of config you would like to do; for the purposes of this demo pick standard. After you have set a user and password for mySQL you can execute the config wizard.
</p>
<br />

<h3>Step 8: Register PHP within IIS</h3>
<p>
<img width="826" height="863" alt="Screenshot 2026-06-23 020333" src="https://github.com/user-attachments/assets/03cb3a3b-dc1f-4a5b-b03e-8f7c71ce3903" />
<img width="1178" height="706" alt="Screenshot 2026-06-23 020456" src="https://github.com/user-attachments/assets/2c17f223-3a34-439d-9855-cba34a807e14" />
</p>
<p>
Open Internet Information Services Manager as administrator. Once open navigate to PHP Manager and click register new PHP version. The .exe file necessary will be found within your PHP directory on your C: drive. After you have registered the PHP simply restart the IIS server at the home page under Actions>Manage Server. 
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
Using the link in the prereqs download osTicket by following the steps on the website specific to your installation type. Once downloaded unzip the file onto your computer and copy the upload folder into C: \inetpup\wwwroot. After you have copied the folder into wwwroot you must rename it exactly osTicket otherwise osTicket will not work. Now that you have successfully changed the name you can restart the IIS server once again; ff done correctly it should look like the last screenshot above.
</p>
<br />

