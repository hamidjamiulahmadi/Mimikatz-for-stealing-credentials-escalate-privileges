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
<img src="https://i.imgur.com/nRj3t7D.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />

 Then with the help of msfconsole I will set the payload to the local port and local host of my computer and send it to the target victim.
<p align="center">
Running msfconsole metasploit: <br/>
<img src="https://i.imgur.com/nwO4W52.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
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
