<p align="center">
<img src="https://i.imgur.com/Clzj7Xs.png" alt="osTicket logo"/>
</p>

<h1>osTicket - Prerequisites and Installation</h1>
This tutorial outlines the prerequisites and installation of the open-source help desk ticketing system osTicket.<br />


<h2>Environments and Technologies Used</h2>

- Microsoft Azure (Virtual Machine with 4cpus)
- Remote Desktop
- Internet Information Services (IIS)

<h2>Operating Systems Used </h2>

- Windows 10 Pro</b>

<h2>List of Prerequisites</h2>

- PHP Manager for IIS
- Rewrite Module
- PHP 7.3.8
- VC_redist.x86.exe
- MySQL 5.5.62
- HeidiSQL
- osTicket-v1.15.8.zip

<h2>Installation Steps:</h2>

- Install / Enable IIS in Windows with CGI and Common HTTP Features. Observations/Notes: ISS (It's a web server that allows the computer to serve up websites). osTicket runs out of a website and we need to configure ISS in order to run osTicket

![Screenshot 2024-07-04 132507](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/76c2ccae-cc65-419d-9304-3a15c47efcbf)
![Screenshot 2024-07-04 132533](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/c812bf3a-bae0-4795-bdb3-390f6e65c7f6)
![Screenshot 2024-07-04 132650](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/acdf59c7-46b0-4eb3-a913-c851014d6051)
![Screenshot 2024-07-04 132725](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/036d0ac9-9a90-4354-8b49-e6d32e3e27f4)
![Screenshot 2024-07-04 132825](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/72383826-e208-4e98-8c60-a3d397b635f0)
![Screenshot 2024-07-04 132838](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/a1e01946-1d54-4277-8121-f1b2b4446bdb)

- Test Network Service by going to the loop back IP address 127.0.0.1 in the web browser. Observations: A web page should show up that says Internet Information Services. 

![Screenshot 2024-07-04 133434](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/9b497c08-c16d-4249-90e9-5035184492da)

- Download and Install PHP Manager for IIS (PHPManagerForIIS_V1.5.0.msi)

![Screenshot 2024-07-04 132317](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/6a174649-cd78-41df-ad1f-7faabc7db1bb)
![Screenshot 2024-07-04 132932](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/2de62b4f-8a36-4b69-961e-47531218ae2b)

- Download and Install the Rewrite Module (rewrite_amd64_en-US.msi)

![Screenshot 2024-07-04 133304](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/77afd062-f446-4ecf-919f-55826ed06a2e)
![Screenshot 2024-07-04 133320](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/b0c18f34-a8b5-4801-9620-758beb85928a)

- Create a Directory for PHP on the local hard drive.

![Screenshot 2024-07-04 133707](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/8e1deb6e-bd80-4eab-8c60-b5e2e492ba3b)

- Download PHP 7.3.8 (php-7.3.8-nts-Win32-VC15-x86.zip) and unzip the contents into C:\PHP

![Screenshot 2024-07-04 134030](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/3442838e-3a71-41be-954a-d0beb5e33581)
![Screenshot 2024-07-04 134110](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/dda61fba-5588-4c4f-abec-bc04ddb34fb8)

- Download and Install VC_redist.x86.exe.

![Screenshot 2024-07-04 134244](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/c365285f-116f-4483-b2e9-65782cd7fee5)
![Screenshot 2024-07-04 134255](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/257a7cef-9275-407d-b688-762cb5dc20ef)

- Download and Install MySQL 5.5.62 (mysql-5.5.62-win32.msi). Observations/Notes: Do a typical Install. After Installation is finished, select Standard Configuration. Create a password for root and execute it. What this will do is install a database on the computer because osTicket needs a database to store tickets,users, etc.

![Screenshot 2024-07-04 134409](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/18374980-b4b8-413f-84ea-093a1b40929a)
![Screenshot 2024-07-04 134441](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/bf595655-a22d-457e-a1ad-8064a6300546)
![Screenshot 2024-07-04 134456](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/d5bd7c13-7d51-4493-b9fd-1bfd31b602ec)
![Screenshot 2024-07-04 134519](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/b9578753-2520-476a-b361-bf9aba16e4cd)
![Screenshot 2024-07-04 134519](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/43f5206c-492f-46e8-bef9-b88aa19f2858)
![Screenshot 2024-07-04 134701](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/31a381ac-8fdd-401d-b9eb-0137fce2aa11)
![Screenshot 2024-07-04 134724](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/d1d2462b-32ea-4eed-b618-a658de188e9a)

- Open IIS as an Admin

![Screenshot 2024-07-04 134807](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/5f1b0c4c-37b4-4b0f-9a73-799fa9ac4467)

- Register new PHP by going to the PHP folder that was created in the local hard drive. Select php-cgi. Observations: Whatever activity you do inside the ISS, it is recommended to restart the web server, first by clicking on the server name and clicking restart.

![Screenshot 2024-07-04 134842](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/3d56b9e2-c602-47a8-b133-11d6c1ff8ec4)
![Screenshot 2024-07-04 134901](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/f48eaaf7-7395-474c-a651-3ef6d14dd6b9)
![Screenshot 2024-07-04 134943](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/1af13498-d08e-486f-8ce0-846df8f3b504)
![Screenshot 2024-07-04 134954](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/baa9a949-fbc4-4929-a19b-1525654e5878)
![Screenshot 2024-07-04 135030](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/db5cacd4-683e-46e9-bd59-8bed51b1d529)

- Download / Extract osTicket v1.15.8 in the download folder.

![Screenshot 2024-07-04 185552](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/a3081349-e2db-45d1-ac10-47dfce029f21)

- Copy “upload” folder to c:\inetpub\wwwroot

![Screenshot 2024-07-04 135627](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/c2e28f8c-f6fa-40e4-939e-eab11b4ced0b)

- From within c:\inetpub\wwwroot, Rename “upload” to “osTicket”

![Screenshot 2024-07-04 135839](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/c8d46173-8c7f-4c44-9527-8081418209b5)

- Reload ISS by restarting the server

![Screenshot 2024-07-04 135030](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/84938554-b59d-4002-b249-4693d185357d)

- Go to sites > Default > osTicket, On the right, click “Browse *:80”. Observations: Note that some extensions are not enabled.

![Screenshot 2024-07-04 141641](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/9c317d79-f811-4a9f-8533-854e445a1876)
![Screenshot 2024-07-04 141648](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/8ef04be5-4c2c-485d-9e5a-4d48595d8323)

- Enable extensions: php_imap.dll / php_intl.dll / php_opcache.dll.

![Screenshot 2024-07-04 141754](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/30df1b53-56c9-4809-bff6-a697e4bae933)
![Screenshot 2024-07-04 141902](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/64c01683-084a-4017-8b6a-82a295cf6ed6)

- Go back to the osTicket browser and refresh it. Observations: you will see more extensions being enabled.

![Screenshot 2024-07-04 141917](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/01fb1338-4129-4721-8b43-7ddab34cec03)

- Rename: "ost-sampleconfig.php" to "ost-config.php" from within C:\inetpub\wwwroot\osTicket\include\ost-sampleconfig.php

![Screenshot 2024-07-04 142041](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/e579a9f7-ca83-4f6d-90b0-dddedbc74d5b)
![Screenshot 2024-07-04 142107](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/e008d95f-d014-4816-9047-35278bf90e4e)

- Assign Permissions: ost-config.php. Disable inheritance > Remove All New Permissions / Everyone > All

![Screenshot 2024-07-04 142209](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/51ee2a3e-163f-4631-9922-68749db0a057)
![Screenshot 2024-07-04 142304](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/9e762de3-2f1f-4692-af77-f3efb9723a41)
![Screenshot 2024-07-04 142313](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/0aaaea0a-ad87-4449-8454-5012e3d59f55)
![Screenshot 2024-07-04 142337](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/5eb29aa6-e262-4b46-8522-aab5720f2bc3)
![Screenshot 2024-07-04 142409](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/4080194f-ac31-4927-91b2-459796443d99)
![Screenshot 2024-07-04 142421](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/00154977-693f-4f47-a994-52a420197be2)

- Continue setting up osTicket in the browser by clicking continue.

![Screenshot 2024-07-04 141917](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/f7e91c24-3f65-4da1-8779-720b7550a310)

- Fill in the information for System settings and Admin User for now.

![Screenshot 2024-07-04 142737](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/c2a5c3a9-6c70-496b-b3aa-9bbe0d0488e8)

- Download and Install HeidiSQL. Observations: Heidi SQL will allow us to connect to the SQL database. This is basically a client database where we can interact with it.

![Screenshot 2024-07-04 142847](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/84b0d18d-5757-47f0-ab55-e3eca06630f0)
![Screenshot 2024-07-04 142931](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/e3656ac2-e58e-4421-ae1b-234e4293133c)

- Open Heidi > Create a new session > Type the password for root > Open

![Screenshot 2024-07-04 142952](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/2d17e49f-dcb7-4f43-a05c-b2358273d5fa)
![Screenshot 2024-07-04 193654](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/355d713d-fb09-4292-b3ac-113c3de12fac)
![Screenshot 2024-07-04 143309](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/663d0007-13ca-4092-b2b2-b46faba0080b)
![Screenshot 2024-07-04 143349](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/f7864bef-dee2-403b-a3a7-3338ed596ff5)

- Finish Setting up osTicket in the browser by filling the Database settings.

![Screenshot 2024-07-04 143458](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/c6dacced-1e30-4e39-89b3-18161d763484)
![Screenshot 2024-07-04 143517](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/21492804-7325-4140-bce2-fc090fb10d2b)

- Clean up by Deleting folder : C:\inetpub\wwwroot\osTicket\setup

![Screenshot 2024-07-04 143633](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/8a3a6ae3-8522-4507-b3b5-99d58c84f0f0)

- Set Permissions to “Read” only in: C:\inetpub\wwwroot\osTicket\include\ost-config.php

![Screenshot 2024-07-04 143755](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/c08cdfb4-8f5a-4817-b8fc-fa253d60b86e)
![Screenshot 2024-07-04 143832](https://github.com/erik-salgado/osticket-prereqs/assets/173113320/e8316afe-5115-40a1-84b4-c08e36083745)

osTicket Successfully Installed! Thank you for watching :)
