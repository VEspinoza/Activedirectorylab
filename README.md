<h1>Active Directory Lab</h1>

<h2>Description</h2>
Project consists of creating a simple Active Directory environment through Oracle Virtual Box. Our domain controller, DHCP server, and DNS server will be on a Windows Server 2019 machine. We will create a sample set of user accounts with a name list of randomly generated names and Powershell to automatically create these accounts. We will also create a Windows 10 client machine to connect to the domain and log in with a user account. 
<br />


<h2>Languages and Utilities Used</h2>

- <b>PowerShell</b> 
- <b>Virtual Box</b>

<h2>Environments Used </h2>

- <b>Windows 10</b>
- <b>Windows Server 2019</b>

<h2>Program walk-through:</h2>
Our Windows Server 2019 virtual machine will be configured with 2 NICs. One to access the internet and one for our internal network. It will act as our Domain Controller, DHCP server, and a DNS server.
<br/>
<br/>

<p align="center">
Configuration of internal NIC (Internet NIC can be left as is): <br/>
<img src="https://i.imgur.com/X4mPE9c.png" height="80%" width="80%" alt="VirtualBox Setup"/>
<br />
<br />
After configuring the NIC we can add the DC role onto the server and create a forest for our domain 'mydomain.com' <br/>
<br/>
Creating our forest (default DC options can be used):  <br/>
<img src="https://i.imgur.com/kwt3Sha.png" height="80%" width="80%" alt="VirtualBox Setup"/>
<br />
<br />
Then we can setup routing so that we can use our DHCP server. <br/>
<br/>
Make sure to set NAT for configuration: <br/>
<img src="https://i.imgur.com/HyNrNyS.png" height="80%" width="80%" alt="VirtualBox Setup"/>
<br/>
<br/>
And set the internet NIC as our public interface: <br/>
<img src="https://i.imgur.com/TQrsHaS.png" height="80%" width="80%" alt="VirtualBox Setup"/>
<br />
<br />
Next we can setup our DHCP server. <br/><br/>
Start by setting a name and scope range: <br/>
<img src="https://i.imgur.com/LyIy21Q.png" height="80%" width="80%" alt="VirtualBox Setup"/>
<br />
<br />
Set IP range:  <br/>
<img src="https://i.imgur.com/n65jVeh.png" height="80%" width="80%" alt="VirtualBox Setup"/>
<br />
<br />
Set our gateway:  <br/>
<img src="https://i.imgur.com/bwQ3ZIH.png" height="80%" width="80%" alt="VirtualBox Setup"/>
<br />
<br />
Confirm our DHCP service is working:  <br/>
<img src="https://i.imgur.com/eFOFDDG.png" height="80%" width="80%" alt="VirtualBox Setup"/>
<br />
<br />
Place holder heading:  <br/>
<img src="https://i.imgur.com/" height="80%" width="80%" alt="VirtualBox Setup"/>
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
