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

- Windows 10</b> (21H2)

<h2>List of Prerequisites</h2>

- Azure Virtual Machine
- osTicket Installation Files
- IIS
- RDP

<h2>Installation Steps</h2>

  Download the osTicket installation files using this link: https://drive.google.com/uc?export=download&id=1b3RBkXTLNGXbibeMuAynkfzdBC1NnqaD . Then unzip it on your desktop.
</p>
<br />

<p>
<img <img width="471" height="587" alt="image" src="https://github.com/user-attachments/assets/40e1af43-db4a-42b4-b52e-7645abc41cd5" />

</p>
<p>
Open up the control panel -> under "Programs" click "Uninstall a program" -> "Turn Windows features on or off". Enable Internet Information Services (IIS), World Wide Web Services -> click "CGI".
</p>
<br />

<p>
<img <img width="241" height="58" alt="image" src="https://github.com/user-attachments/assets/2cb498e5-9bb8-4cc2-b3b8-5856bdd40346" />

</p>
<p>

</p>
<br />

<p>
<img <img width="229" height="62" alt="image" src="https://github.com/user-attachments/assets/2d67dd8c-7f09-435c-9bba-aa1a59421738" />


</p>
<p>

</p>
<p>

</p>
<br />

<p>
<img <img width="576" height="222" alt="image" src="https://github.com/user-attachments/assets/e7627a4b-778b-4fc9-8114-55f1fce7587b" />

</p>
<p>

</p>
<br />

<p>
<img <img width="398" height="293" alt="image" src="https://github.com/user-attachments/assets/f3b60f9c-5d17-4641-ae08-2d5b3cb001a9" />

</p>
<p>
  
Go to your osTicket Install Files folder and install the IIP extensions named "PHPManagerForIIS" and "rewrite_amd64". 

 <p>
<img <img width="430" height="364" alt="image" src="https://github.com/user-attachments/assets/802971f4-ce2a-4d7c-9cca-bf92b3035ec0" />

</p>
<p>

Create a folder named "PHP" on the Windows (C:) drive. Then extract the "php-7.3.8" folder from the osTicket Install folder into C:/PHP.

 <p>
<img <img width="1420" height="917" alt="image" src="https://github.com/user-attachments/assets/01cb7e8d-526e-4afa-bf5a-923422b852eb" />



</p>
<p>
  
Install the "VC_redist.x86" extension.
</p>
<br />

<p>
<img <img width="534" height="367" alt="image" src="https://github.com/user-attachments/assets/88c99af0-01e1-45f5-9306-8822629aef34" />

</p>
<p>
Install the "mysql-5.5.62" extension. Use these settings: "Typical Setup" -> "Standard Configuration". Next, modify security settings. For this example, the username and password will BOTH be "root". Execute the configuration.
</p>
<br />

<p>
<img <img width="618" height="467" alt="image" src="https://github.com/user-attachments/assets/cee81203-6d83-45a0-8522-dda74333195d" />

</p>
<p>

</p>
<br />

<p>
<img <img width="628" height="467" alt="image" src="https://github.com/user-attachments/assets/249f3eee-114c-424a-927d-743b51f06309" />


</p>
<p>

</p>
<br />

<p>
<img <img width="609" height="463" alt="image" src="https://github.com/user-attachments/assets/6446fb7e-4282-4f7a-bcee-08a99905b3f1" />

</p>
<p>
  
</p>
<br />

<p>
<img <img width="630" height="470" alt="image" src="https://github.com/user-attachments/assets/1f0368fd-f655-498f-ad77-0575dedf02b8" />


</p>
<p>

</p>
<br />

<p>
<img <img width="627" height="478" alt="image" src="https://github.com/user-attachments/assets/d99981f6-b393-4ed1-a57d-a9105d10b90d" />

</p>
<p>

Run IIS as administrator. Register PHP within IIS. PHP Manager -> Register new PHP, click the 3 dots -> C:\PHP\php-cgi.exe . Reload IIS by opening IIS, stopping and starting the server.

</p>
<br />

<p>
<img <img width="934" height="505" alt="image" src="https://github.com/user-attachments/assets/aa651b57-6bfe-4617-ae67-51e0b3942fed" />

</p>
<p>

</p>
<br />

<p>
<img <img width="873" height="303" alt="image" src="https://github.com/user-attachments/assets/6722a3d8-692a-4bbc-ae4e-2e0f866df715" />


</p>
<p>

</p>
<br />

<p>
<img <img width="621" height="259" alt="image" src="https://github.com/user-attachments/assets/28f03597-3f17-4732-9c7d-d7c2a29fe55b" />


</p>
<p>

  </p>
<br />

<p>
<img <img width="928" height="579" alt="image" src="https://github.com/user-attachments/assets/85c4e432-f908-49dd-b675-967aa25e68a3" />



</p>
<p>

  </p>
<br />

<p>
<img <img width="376" height="223" alt="image" src="https://github.com/user-attachments/assets/9c0f4373-cde8-44a2-80b1-8659f000b688" />

</p>
<p>
From the osTicket Install Files folder, extract “osTicket-v1.15.8.zip", then copy the upload folder into “c:\inetpub\wwwroot”, then rename the folder "osTicket."
</p>
<br />

<p>
<img <img width="1434" height="336" alt="image" src="https://github.com/user-attachments/assets/5ed5c761-ab9d-4b60-ab1f-6d3a6821f588" />
</p>
<p>
Now go to sites -> default web site -> osTicket, on the right side, click "Browse *:80”. You'll notice some extensions are disabled, so we need to go back and enable the ones we need.
</p>
<br />

<p>
<img <img width="1342" height="167" alt="image" src="https://github.com/user-attachments/assets/88f5a392-19a7-4dc1-bab1-3b0985aa7cc9" />

<img width="400" height="487" alt="image" src="https://github.com/user-attachments/assets/26cdbfa0-130d-4ea1-a816-5c125edc94a0" />

Back on IIS on the same osTicket folder, go to PHP Manager. Scroll down and click "Enable or disable an extension" and enable these extensions: "php_imap.dll", "php_intl.dll", and "php_opcache.dll". Then refresh the osTicket site on your browser.

<img width="627" height="325" alt="image" src="https://github.com/user-attachments/assets/9a0865d1-5e25-4ab8-b2d2-416f3af71728" />

<img width="456" height="170" alt="image" src="https://github.com/user-attachments/assets/ea891cb7-0880-4935-adee-7b297fde330d" />

<img width="345" height="272" alt="image" src="https://github.com/user-attachments/assets/3ff61fce-ac12-413b-b26e-25a57c7d7d0a" />

</p>
<p>
Rename the "ost-sampleconfig.php" from "C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php" to "C:\inetpub\wwwroot\osTicket\include\ost-config.php". Assign permissions within ost-config.php by right clicking -> properties -> security. Then disable inheritance -> Remove All and then New Permissions -> Everyone -> All.
</p>
<br />

<img width="738" height="635" alt="image" src="https://github.com/user-attachments/assets/4722616e-c429-4b48-9a92-89bd0a440b30" />

<img width="480" height="631" alt="image" src="https://github.com/user-attachments/assets/9579af43-9d77-40f7-8fcc-431134324466" />

