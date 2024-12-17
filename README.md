<h1>Mimikatz-for-stealing-credentials-escalate-privileges</h1>

<h2>Description</h2>
Mimikatz is a post exploitation tools that enables users to save and view authentication credentials such as kerebos tickets, dump passwords  from memory, PINs, as well as hashes. It enables you to preform functions such as pass-the-hush, pass-the-ticket, and makes post-exploitation lateral movement within a network. 

In this project i will create a backdoor file and then i will share it with the victim machine to stablish a connection, after getting access to the victim machine, i will bypassing the user account control of the Windows 10 with the help of msfconsole to gain access of the root user, furthermore i will run Mimikatz to get the NTLM of the Admin user and after that i will change the admin user password and at the end testing the lab.
<br />


<h2>Environments Used </h2>

- <b>Parrot Operating System</b> 
- <b>Windows 10</b>

<h2>Lab walk-through:</h2>

<p align="center">
Creaing backdoor and sharing path: <br/>
<img src="https://i.imgur.com/nRj3t7D.png" height="80%" width="80%" alt="Lab Steps Nr.1"/>
<br />

 Then with the help of msfconsole I will set the backdoor file to the local port and local host of my computer and send it to the target victim.
<p align="center">
Running msfconsole metasploit: <br/>
<img src="https://i.imgur.com/nwO4W52.png" height="80%" width="80%" alt="Lab Steps Nr.2"/>
<br />


<p align="center">
Victim machine got the file: <br/>
<img src="https://i.imgur.com/b9ILAnK.png" height="80%" width="80%" alt="Lab Steps Nr.3"/>
<br />

<p align="center">
now the connection is stablished and i have access to the target machine but as you see at the bottom i have a normal user access previlidge: <br/>
<img src="https://i.imgur.com/DQnlWC0.png" height="80%" width="80%" alt="Lab Steps Nr.4"/>
<br />

<p align="center">
now i will bypass the windows UAC protection via the Fodhelper-registry key: <br/>
<img src="https://i.imgur.com/QZTO7ZY.png" height="80%" width="80%" alt="Lab Steps Nr.5"/>
<br />

<p align="center">
here i have bypassed the windows UAC protection and now I got the root user as you see at the bottom.: <br/>
<img src="https://i.imgur.com/BVtUmv5.png" height="80%" width="80%" alt="Lab Steps Nr.6"/>
<br />

<p align="center">
Now I will load the Mimikatz and then I will see what type of option I can run on the target machine to get hushes,first I will try to load the NTML Hash of all users of Windows.: <br/>
<img src="https://i.imgur.com/ty2Mr06.png" height="80%" width="80%" alt="Lab Steps Nr.7"/>
<img src="https://i.imgur.com/e1oLgOM.png" height="80%" width="80%" alt="Lab Steps Nr.7"/>
 <img src="https://i.imgur.com/HH37VsA.png" height="80%" width="80%" alt="Lab Steps Nr.7"/>
<br />

 
<br />

</p>

<!--
 ```diff
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
