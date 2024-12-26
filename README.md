<h1>Mimikatz-for-stealing-credentials-escalate-privileges</h1>

<h2>Goal</h2>
<br />In this lab i will create a backdoor file and then i will share it with the victim machine to stablish a connection, after getting access to the victim machine, i will bypassing the user account control of the Windows 11 with the help of Metasploit to gain access of the root user, furthermore i will run Mimikatz to get the NTLM of the Admin user and after that i will change the admin user password and at the end testing the lab.<br />

<br />Mimikatz is a post exploitation tools that enables users to save and view authentication credentials such as kerebos tickets, dump passwords  from memory, PINs, as well as hashes. It enables you to preform functions such as pass-the-hush, pass-the-ticket, and makes post-exploitation lateral movement within a network. 
<br />


<h2>Environments Used </h2>

- <b>Parrot Operating System</b> 
- <b>Windows 11</b>

<h2>Lab walk-through:</h2>

<p align="center">
Step Nr.1 : Creaing backdoor and sharing path: <br/>
<img src="https://i.imgur.com/nRj3t7D.png" height="80%" width="80%" alt="Lab Steps Nr.1"/>
<br />

Steps Nr.2 : Then with the help of msfconsole I will set the backdoor file to the local port and local host of my computer and send it to the target victim.
<p align="center">
Running msfconsole metasploit: <br/>
<img src="https://i.imgur.com/nwO4W52.png" height="80%" width="80%" alt="Lab Steps Nr.2"/>
<br />


<p align="center">
Steps Nr.3: Victim machine got the file: <br/>
<img src="https://i.imgur.com/b9ILAnK.png" height="80%" width="80%" alt="Lab Steps Nr.3"/>
<br />

<p align="center">
Steps Nr.4: now the connection is stablished and i have access to the target machine but as you see at the bottom i have a normal user access previlidge: <br/>
<img src="https://i.imgur.com/DQnlWC0.png" height="80%" width="80%" alt="Lab Steps Nr.4"/>
<br />

<p align="center">
Steps Nr.5: now i will bypass the windows UAC protection via the Fodhelper-registry key: <br/>
<img src="https://i.imgur.com/QZTO7ZY.png" height="80%" width="80%" alt="Lab Steps Nr.5"/>
<br />

<p align="center">
Steps Nr.6: here i have bypassed the windows UAC protection and now I got the root user as you see at the bottom.: <br/>
<img src="https://i.imgur.com/BVtUmv5.png" height="80%" width="80%" alt="Lab Steps Nr.6"/>
<br />

<p align="center">
Steps Nr.7: Now I will load the Mimikatz and then I will see what type of option I can run on the target machine to get hushes,first I will try to load the NTML Hash of all users of Windows.: <br/>
<img src="https://i.imgur.com/ty2Mr06.png" height="80%" width="80%" alt="Lab Steps Nr.7"/>
<img src="https://i.imgur.com/e1oLgOM.png" height="80%" width="80%" alt="Lab Steps Nr.7"/>
 <img src="https://i.imgur.com/HH37VsA.png" height="80%" width="80%" alt="Lab Steps Nr.7"/>
<br />

 <p align="center">
Steps Nr.8: As you see, I got all the users' credentials. Then, I will try to do a further search on the target machine and change the admin password of the target machine.: <br/>
<img src="https://i.imgur.com/HH37VsA.png" height="80%" width="80%" alt="Lab Steps Nr.8"/>
<br />

   <p align="center">
Steps Nr.9: In the picture above you see i got the NTLM hashes of the Admin user, now i will chage the NTLM of the administrator and set a new password for the admin account.: <br/>
<img src="https://i.imgur.com/UgPLFn7.png" height="80%" width="80%" alt="Lab Steps Nr.9"/>
<img src="https://i.imgur.com/3Csum3R.png" height="80%" width="80%" alt="Lab Steps Nr.9"/>
<img src="https://i.imgur.com/Eh8Ik5P.png" height="80%" width="80%" alt="Lab Steps Nr.9"/>
<br />
 <p align="center">
Steps Nr.10: We can observe that the password has been change and the Admin account has new NTLM credentials, Now we will try on login with new password for the lab testing.: <br/>
<img src="https://i.imgur.com/FDSxIe9.png" height="80%" width="80%" alt="Lab Steps Nr.10"/>
<img src="https://i.imgur.com/uUYcglp.png" height="80%" width="80%" alt="Lab Steps Nr.10"/>
<br />
Accomplishment: As you see, i have successfully loged in to the victim machine with new password and the lab is completed successfully. 
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
