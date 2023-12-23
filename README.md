<p align="center">
<img src="https://imgur.com/77CNWfe.png" alt="Nessus"/>
</p>

<h1>Utilizing Nessus to Perform Vulnerability Scan</h1>
In this tutorial, we set up a Windows 10 ISO in VMWare to perform vulnerability scans <br />

<h2>Environments and Technologies Used</h2>

- VMWare Player
- Windows 10 ISO
- Nessus Vulnerability Scanner

<h2>Operating Systems Used </h2>

- Windows 10 ISO

<h2>High-Level Steps</h2>

- We first downloaded a Windows 10 ISO through Microsoft to set up within a VMWare Workstation
- We then downloaded Nessus Essentials on my local personal computer
- After testing connectivity to the Virtual Machine within VMWare Workstation, we set up Nessus to do a non-credentialed scan
- Once the non-credentialed scan was finished, we then set up a credentialed scan to see the difference / importance
- We then go over a general explanation of the usefullness of Nessus

<h2>Actions and Observations</h2>

<p>
The first thing we did was set up a Windows 10 ISO within the VMWare Workstation and then shut off the Windows Defender Firewall Policy to make this VM as vulnerable as possible. The idea is that we want to see the difference in a scan with / without credentials on a vulnerable system facing the internet. 
  </p>
<p><strong>Windows Defender Firewall</strong></p>
<img src="https://imgur.com/GONGDa6.png" height="80%" width="80%" alt="Windows Defender Policy"/>
</p>
<p>
After we shut off the Windows Defender Firewall, we ran a non-credentialed scan within Nessus to see what vulnerabilities can be seen from a basic "black-box" approach from general internet traffic. This shows that from the "outside looking in" this system seems relatively safe without knowing much more about it.</p>
<br />

<p>
<img src="https://imgur.com/Q9i4grO.png" height="80%" width="80%" alt="non-cred"/>
</p>
<br>
<p>
After the non-credentialed scan, we did a credential scan of the same exact VM and we can see there is a significant difference in known vulnerabilities. This makes sense as the credentialed scan would show the opporutnites that are available from inside the system itself. This would be comparable to the level a System Administrator would have with "Administrator / Root" access. On the other hand, this also shows what a hacker would see if they were able to break into the system and utilize privelege escalation techniques to access one of these Administrator / root accounts. 

<img src="https://imgur.com/ZY5mLoh.png" height="80%" width="80%" alt="logs"/>

</p>
<br />
<p>
We then checked on the "Critical" Vulnerabilities that were found within this Nessus scan and we can see that there are an incredible amount of vulnerabilities within the "Critical" and "High" levels. This indicates vulnerabilities that should take very high priority to patch and mitigate to avoid any potential issues of malicious attackers trying to cause issues within this virtual machine. Depending on the vulnerability, this could also lead to escalation into other systems within the "enterprise" network if ignored. 
<img src="https://imgur.com/GlVkthw.png" height="80%" width="80%" alt="Middle"/>
</p>
<p>
The last screenshot shows that if you click on the specific vulnerability itself, you can see that there is quite a bit of information. You can see the description of the error, the solution to the vulnerability, a "See Also" section that direcrtly links to a better, in depth explanation, and much more. Nessus seems to be a security tool that should be integral to anyone's arsenal to run continued vulnerability scans in order to best protect the company from malicious intruders. 
<img src="https://imgur.com/GtHlvZD.png" height="80%" width="80%" alt="Last"/>
</p>
<br />
