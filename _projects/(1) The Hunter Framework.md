---
name: The Hunter Framework
tools: [Python 3.0, Bash]
image: https://wallpapercave.com/wp/wp5709451.jpg
description: An All in One Pentesting Framework for Ethical Hackers & Penetration Testers
---
![Hunter](https://raw.githubusercontent.com/gsvprharsha/Hunter-Framework/main/imgs/Hunter-Framework.png)


## Important Note
This tool is for educational and ethical practices only. The developers are not responsible if the tool is misused by an individual

## About Hunter
Hunter is a penetration testing framework for ethical hackers to use in their tests. As of now, Hunter consists of 5 different tools for the user. The tools are listed as follows:
  <li>Port Scanner</li>
  <li>SSH Bruteforce</li>
  <li>Backdoor Manager</li>
  <li>Password cracker</li>
  <li>Network Scanner</li>
  <li>Wordlist Generator</li><br>
  
More tools are to be added very soon.

## Features (as of 31/01/2022)
<li>Access it from anywhere by typing "sudo hunter"</li>
<li>6 tools in one.</li>
<li>Port Scanner accepts URLs and multiple targets.</li>
<li>You may add your own set of wordlists to the existing ones using wordlist generator.</li>
<li>A network mapper that shows MAC and IP addressess.</li>


## Tested On
![Kali Linux](https://img.shields.io/badge/Kali_Linux-557C94?style=for-the-badge&logo=kali-linux&logoColor=white)
![Debian](https://img.shields.io/badge/Debian-A81D33?style=for-the-badge&logo=debian&logoColor=white)
![Ubuntu](https://img.shields.io/badge/Ubuntu-E95420?style=for-the-badge&logo=ubuntu&logoColor=white)



## Contributing
<b>Thank you so much for considering to contribute to the Project. Place a pull request and if feasible it will be merged into the main branch of this repository.</b>

## Using Hunter
<b> Hunter aims to be a begineer friendly framework. Using Hunter does not require any advanced skills, but you need to be familiar with some of the terminologies of penetration testing.</b>

## Installation
<b>Note: <br>Make sure to run the framework in root user. Hunter requires some permissions, which are only available to the root user</b><br>
<b> Follow the below steps to run Hunter without any issues on your device.</b>
<li>Open your terminal and clone this repository using the following command</li><br>

```
git clone https://github.com/gsvprharsha/Hunter-Framework.git
```

<li>Change into the downloaded directory. Now make sure you are using the <b>root</b> user</li><br>
<li>Now change the setup.sh file to an executable using the following command.</li><br>

```
chmod +x setup.sh
```

<li>Now run the file</li><br>
```
./setup.sh
```

<li>Wait for the dependencies to get installed</li>
<li>Now after all the dependencies are installed, you can start using the Framework</li>
<li>To run the framework, type the following command in your terminal</li><br>

```
sudo hunter
```

- You should be greeted with the following screen

![Welcome](https://raw.githubusercontent.com/gsvprharsha/Hunter-Framework/main/imgs/Hunter%20Welcome%20Screen.png)

- Now you may choose your option and hit enter, which would ask you input regaring the target, gateway,...etc

## What to expect in future updates
<li>A anonymizing script</li>
<li>An ARP Spoofer</li>
<li>An Email Bomber</li>
<li>Rootkit Generator</li>
And many more tools to come. If you are into building tools, then do contribute to the project.
