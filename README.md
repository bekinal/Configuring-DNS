<h1>DNS Configuration</h1>

<h2>Description</h2>
Project consists of adding and resolving A and CNAME records. This project assumes that a version of Windows Server 2016 is installed, configured with Active Directory Domain Services, and has a Windows 10 client added to its domain. 
<br />


<h2>Utilities Used</h2>

- <b>VirtualBox</b> 
- <b>Windows Server 2016</b>

<h2>Environments Used </h2>

- <b>Windows Server 2016</b>

<h2>Configuring DNS:</h2>

 In the Server Manager Dashboard, select tools and DNS: <br/>
<img src="https://i.imgur.com/ShvbyxP.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Expand "Server1 > Forward Lookup Zones > cyber.local". Right click "cyber.local" and select "New Host (A or AAAA)":  <br/>
<img src="https://i.imgur.com/6f3vTZD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
For name, enter "test-client"; for IP address, enter "10.0.0.10"; and click "Add Host". Click OK when prompted: <br/>
<img src="https://i.imgur.com/qKhyo0r.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Log into the Windows 10 client VM, open the CMD and run the command "nslookup test-client.cyber.local":  <br/>
<img src="https://i.imgur.com/jlxOrvE.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
In the server, go back to the DNS manager and right click the "cyber.local" folder again. This time, select "New Alias (CNAME)":  <br/>
<img src="https://i.imgur.com/ZbIiyHD.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Under Alias name, enter "MY-FAVORITE-CLIENT" and click ok:  <br/>
<img src="https://i.imgur.com/GbtiAZn.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
Click "Browse" then, click "SERVER1" then, "Forward Lookup Zones" "cyber.local" and finally, the "test-client" text file. The Fully qualified domain name for target host should read "test-client.cyber.local":  <br/>
<img src="https://i.imgur.com/5up5UOk.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
</p>
Log into the Windows 10 client and run CMD. Enter the command "nslookup my-favorite-client.cyber.local": <br/>
<img src="https://i.imgur.com/0pr9tMx.png" height="80%" width="80%" alt="Disk Sanitization Steps"/>
