---
name: Br0ther Ey3
tools: [Python 3.0, Bash]
image: https://raw.githubusercontent.com/gsvprharsha/Br0ther_Ey3/main/imgs/BR0THER%20EY3.png
description: An open-source OSINT tool, that can check for an individual's social media accounts on the internet, using status codes; to determine the existence of the profile in that website.
---

![Br0ther](https://raw.githubusercontent.com/gsvprharsha/Br0ther_Ey3/main/imgs/Br0ther_Ey3.png)

# What is Br0ther Ey3

Br0ther Ey3 is an **open-source OSINT tool**, that can be used to **check for an individual's account** on some of the most popular **Social Media websites** on the internet. It uses status codes to determine whether there is an account with the username that is provided to it; on the website.

## Setup
Setting up **Br0ther Ey3** is very simple. You can use it directly from the directory **or** use the `setup.sh` program to install it in such a way that you can access it from anywhere in the system.

```bash
git clone https://github.com/gsvprharsha/Br0ther_Ey3.git
chmod +x setup.sh
sudo ./setup.sh
```

## Usage
To use Br0ther Ey3, execute the following command in your terminal. Just replace `<username>` with the username of your choice.
```bash
broeye -u <username>
```
If you are using it directly from the directory without installing it with `setup.sh` then, you can use the following command to continue using Br0ther Ey3.
```bash
python3 broeye -u <username>
```
## Optional Arguments 
```python
usage: broeye.py [-h] --username USERNAME [--T10] [--t T] [--fbset] [--tiktok] [--tiktok_with_profile_pic]

Br0ther Ey3 OSINT Tool v0.0.2

optional arguments:
  -h, --help            show this help message and exit
  --username USERNAME   Profile Username
  --T10                 Scans only Top 10 websites from list
  --t T                 Take custom number of lists
  --fbset               Scans the websites owned by Facebook
  --tiktok, --tt        Gather information only on tiktok only
  --tiktok_with_profile_pic, --ttwp
                        Tiktok OSINT that also collects the user's profile picture

Embrace The Data :)
```

<p class="text-center">
{% include elements/button.html link="https://github.com/gsvprharsha/Br0ther_Ey3" text="Source Code" %}
</p>
