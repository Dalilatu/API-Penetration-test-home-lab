# API-Penetration-test-home-lab

<h2>Description</h2>
This home lab describes how to set up the perfect home lab for testing APIs
<br />


<h2>Utilities Used</h2>

- <b>Kali Linux</b>


<h2>Environments Used </h2>

- <b>Virtual Box</b>

<h3>Lab Installation Tools</h3>

| Tool Name | Why It Was Used | Download Link |
|-----------|---------------------------|---------------|
| Kali Linux | Offensive security testing and penetration testing distribution. Will be used for our attacks| [Download](https://www.kali.org/get-kali/) |

## Project walk-through:
<h3>Important Configuration</h3><br/>

Once we've installed Kali on Virtual Box, run the following command to update the system. <br/>
`sudo apt update && sudo apt upgrade -y`<br/>
<br/>
Given that <b>Burpsuite</b> will already be installed on Kali, follow these steps to setup your <b>Burpsuite</b> software.<br/>
<br/>
<b>Step 1: Add Extensions</b><br/>
Go to EXTENSION and search for `Autorize`

<p align="center">
<img alt="image" src="https://github.com/user-attachments/assets/9db7588e-f257-4f10-8e00-dad8d398c41c" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

<b>Step 2: Pre configurations to install Autorize extension</b><br/>

<p align="center">
  Download Jython:<br/>
<img  alt="image" src="https://github.com/user-attachments/assets/e7ba6326-53c1-4f2c-870f-0aa546dc5d2f" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

<p align="center">
  Download Jython:<br/>
<img alt="image" src="https://github.com/user-attachments/assets/62266875-7896-4539-9408-372f09a40d04" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
  
<p align="center">
  Go to extension settings on Burpsuite:<br/>
<img alt="image" src="https://github.com/user-attachments/assets/6c8b9110-4bf8-4948-85e4-2fcacf9c4e83" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

<p align="center">
  Search for the Python environment and import the downloaded file there:<br/>
<img alt="image" src="https://github.com/user-attachments/assets/d66a61ba-3026-42db-b6a2-49066617e869" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

<p align="center">
  File imported successfully:<br/>
<img alt="image" src="https://github.com/user-attachments/assets/750042b4-765b-46c6-894c-4c0d6da4deed" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />

<p align="center">
  Go back to BApp on Burpsuite and Install <b>Autorize</b>:
<img alt="image" src="https://github.com/user-attachments/assets/db7894a7-b261-46fc-9f4d-1db7dabc148d" height="80%" width="80%" alt="Disk Sanitization Steps"/>
<br />
<br />
