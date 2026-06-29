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

<b>Step 3: Install the FoxyProxy extension on your browswer</b><br/>

For this lab, we will be using Firefox. <br/>

First go to extension on Firefox and search for FoxyProxy. <br/>

<p align="center">
  Choose FoxyProxy Standard:<br/>
<img alt="image" src="https://github.com/user-attachments/assets/02924768-4d10-4ead-8c53-2b5dff3c5b7f"  height="80%" width="80%"/>
<br />
<br />

Choose FoxyProxy Standard then click on "Add to Firefox". The extension will be added on the bowser but make sure you pin it on toolbar.<br/>
<br/>

<b>Step 4: Configure the proxy</b><br/>

Go to the toolbar and click on the FoxyProxy icon, choose Option and configure your localhost.<br/>

<p align="center">
  Go to foxyproxy and choose `OPtion`:<br/>
<img alt="image" src="https://github.com/user-attachments/assets/ccbba90a-d585-4ed8-a882-b86a6027f25c" height="80%" width="80%"/>
<br />
<br />

<p align="center">
  Go to Proxies and configure localhost listening to port 8080:<br/>
<img alt="image" src="https://github.com/user-attachments/assets/df709eeb-5fbf-4e9d-a783-9eb543654a88" height="80%" width="80%"/>
<br />
<br />

<p align="center">
  Configure localhost listening to port 8080:<br/>
<img alt="image" src="https://github.com/user-attachments/assets/55993248-31eb-4115-bd66-09380dc4cf78" height="80%" width="80%"/>
<br />
<br />

We will then proceed to install a certificate that will enable the communication between the proxy and Burpsuite. For that to be possible, we need to ensure that burpsuite open and the Burp Proxy we just created is chosen. We can then go to this website to get the cetificate.<br/>
`https://burpsuite/cert` <br/>
This will automatically download the certificate. <br/>

Once this is done, go to `settings` in your browser and search for "Certificate"<br/>

<p align="center">
  Search for Cert in settings and click on View cert:<br/>
<img alt="image" src="https://github.com/user-attachments/assets/87f93acf-0404-4705-a9a8-046d9ff854c8" height="80%" width="80%"/>
<br />
<br />

<p align="center">
  Import the cert:<br/>
<img alt="image" src="https://github.com/user-attachments/assets/2c64fb15-bdc5-44a7-bcd2-d9a247808598" height="80%" width="80%"/>
<br />
<br />

Once this is done, you can test the if it works by intercepting the traffic. If the request appears on Burpsuite History tab, then the configuration was successful.<br/>

<br/>
We will also have to add another proxy listening to Postman with Port 5555<br/><br/>

<b>Step 5: Installing Postman</b><br/>


To install Postman, go to your terminal and type the following command:<br/>
<br/>
<h3>Install Postman</h3><br/>
`$ sudo wget https://dl.pstmn.io/download/latest/linux64 -O postman-linux-x64.tar.gz && sudo tar -xvzf postman-linux-x64.tar.gz -C /opt && sudo ln -s /opt/Postman/Postman /usr/bin/postman`<br/>

<br/>
<h3>Install Git</h3>h3></h3><br/>
`$ sudo apt-get install git`<br/>
<br/>

 

<h>Install Docker</h3> <br/>

`$ sudo apt install docker.io -y` <br/>

`$ sudo apt-get install docker.io docker-compose` <br/>
<br/>
 

<h3>Install mitmproxy2swagger</h3><b/>
`$ git clone https://github.com/alufers/mitmproxy2swagger.git` <br/>
`$ cd mitmproxy2swagger` <br/>
`$ sudo docker build -t mitmproxy2swagger.` <br/>
 <br/>

<h3>Install Go</h3><br/>
`$ sudo apt install golang-go` <br/>
<br/>
 

<h3>The JSON Web Token Toolkit v2</h3>
`$ cd /opt` <br/>

`$ sudo git clone https://github.com/ticarpi/jwt_tool` <br/>

`$ cd jwt_tool` <br/>

`$ python3 -m pip install -r requirements.txt --break-system-packages` <br/>


<h3>(Optional) Make an alias for jwt_tool.py</h3>

`$ sudo chmod +x jwt_tool.py`<br/>

`$ sudo ln -s /opt/jwt_tool/jwt_tool.py /usr/bin/jwt_tool`<br/>
<br/>
 

<h3>Install Sublime Text</h3><br/>
<h3>Install the GPG key:</h3><br/>

`$ wget -qO - https://download.sublimetext.com/sublimehq-pub.gpg | gpg --dearmor | sudo tee /etc/apt/trusted.gpg.d/sublimehq-archive.gpg > /dev/null`<br/>

<h3>Select the Stable channel:</h3>

`$echo "deb https://download.sublimetext.com/ apt/stable/" | sudo tee /etc/apt/sources.list.d/sublime-text.list`<br/>

<h3>Update apt sources and install Sublime Text:</h3><br/>

`$sudo apt-get update`<br/>

`$sudo apt-get install sublime-text`<br/>
<br/>

 

<h3>Install Kiterunner</h3><br/>
`$ sudo git clone  https://github.com/assetnote/kiterunner.git`<br/>

`$ cd kiterunner`<br/>

`$ sudo make build`<br/>

`$ sudo ln -s /opt/kiterunner/dist/kr /usr/bin/kr`<br/>
<br/>

 

<h3>Install Arjun</h3><br/>
`$ sudo git clone https://github.com/s0md3v/Arjun.git`<br/>

Recommended way to install arjun:

`$ cd Arjun`<br/>

`$ pip3 install arjun`<br/>

For new kali versions, you can use this method as this error message can appear.<br/>

<p align="center">
  Error message:<br/>
<img alt="image" src="https://github.com/user-attachments/assets/0921037b-0411-48c0-be30-6d7f1e63afc4" height="80%" width="80%"/>
<br />
<br />

Use this method to complete the installation of Arjun.<br/>
`sudo apt update`<br/>
`sudo apt install pipx`<br/>
`pipx install arjun`<br/>
<br/>

 <h3>Install OWASP ZAP</h3><br/>
`$ sudo apt install zaproxy`<br/>

[Link to download Zaproxy](https://www.kali.org/tools/zaproxy/)<br/>

Once ZAP is installed, make sure to navigate to the Manage Add-Ons (CTRL+U). Make sure to apply updates for the Fuzzer and OpenAPI Support.<br/>
<br/>

 

<h3>Useful Wordlists</h3><br/>
[SecLists](https://github.com/danielmiessler/SecLists)<br/>

`$ sudo wget -c https://github.com/danielmiessler/SecLists/archive/master.zip -O SecList.zip \
&& sudo unzip SecList.zip \
&& sudo rm -f SecList.zip`<br/><br/>

<h3>Hacking-APIs (https://github.com/hAPI-hacker/Hacking-APIs)</h3><br/>

`$ sudo wget -c https://github.com/hAPI-hacker/Hacking-APIs/archive/refs/heads/main.zip -O HackingAPIs.zip \
&& sudo unzip HackingAPIs.zip \
&& sudo rm -f HackingAPIs.zip`
