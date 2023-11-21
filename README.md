<h1>Managing Technical Vulnerabilities</h1>



<h2>Description</h2>
In this lab, I employ the Nmap Scripting Engine (NSE) to initiate a vulnerability scan across an entire network, aiming to identify particular vulnerabilities. Utilizing the Greenbone Vulnerability Management framework (formerly known as OpenVAS), I conduct a comprehensive scan on a specific host to detect all potential vulnerabilities outlined in the scanner's dictionary. Subsequently, I record the associated risk entries for each identified vulnerability in SimpleRisk.<br />


<h2>Languages and Utilities Used</h2>

- <b>Nmap Scripting Engine (NSE)</b>
- <b>Greenbone Vulnerability Management framework (OpenVas)</b>
- <b>SimpleRisk</b>
- <b>CVSS-based risk assessment</b>
- <b>NIST 800-40 </B>

<h2>Environments Used </h2>

-  <b>vWorkstation</b> (Windows Server 2019)
-  <b>TargetWindows01</b> (Windows Server 2016) [Domain Controller]
-  <b>Kali</b> (Kali Linux)
-  <b>SimpleRisk</b> (Linux)

<h2>Performing a Vulnerability Scan with Nmap:</h2>

<p align="center">
type Nmap your IP address (172.30.0.0/24) -n --script ftp-anon -p 21 > press Enter to start the Nmap vulnerability scan. We found one machine (172.30.0.3) that has the anonymous vulnerability and has port 21 open. <br/>
<br />
<img src="https://i.imgur.com/UTVPur2.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<br />
<br />
 
<p align="center">
We are going to exploit it to see what we find. Type: ftp 172.30.0.3 (or IP address of the vulnerable machine). after it will ask you for a name and you Type: anonymous 
<br/>
<br />
<img src="https://i.imgur.com/Flq1jhz.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<br />
<br />

<p align="center">
After it will ask you for a name and you will Type: anonymous and then it will ask you for a password where you can type anything
<br/>
<br />
<img src="https://i.imgur.com/Flq1jhz.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<br />
<br />

<p align="center">
The anonymous login is not a problem on its own, but it can quickly become very problematic if sensitive documents are being shared over that FTP service. but in this case, we found a file called newhire.txt. we will grab the file and open it by typing: cat newhire.txt
<br/>
<br />
<img src="https://i.imgur.com/7ov46kV.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<br />
<br />

<h2>Performing a Vulnerability Scan with the GVM Framework:</h2>

<p align="center">
Upon identifying the FTP vulnerability, the next step involves conducting a scan specifically targeting the vulnerable machine. <br/>
<br />
<img src="https://i.imgur.com/lt0k27d.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<br />
<br />
 

<h2>Documenting Vulnerabilities with SimpleRisk:</h2>

<p align="center">
After doing the scan we will document the finding using SimpleRisk and patch them according to the severity score. <br/>
<br />
<img src="https://i.imgur.com/sdGHINw.png" height="70%" width="70%" alt="Disk Sanitization Steps"/>
<br />
<br />
 




<!--
 ```dif
- text in red
+ text in green
! text in orange
# text in gray
@@ text in purple (and bold)@@
```
--!>
