# PITA-commands-and-setups
Collection of pain in the ass commands which take a bit of googling to find the successful setup





```Installing jdk-8 in kali 2020.X```
- $ sudo apt-get install openjdk-8-jdk
- $ echo "deb http://ftp.us.debian.org/debian sid main" >> /etc/apt/sources.list
- $ apt-get update && apt-get upgrade
- $ sudo apt-get install openjdk-8-jdk
- $ sudo update-alternatives --config java



```linux b64 -> NT utf-16le b64```
- $ echo 'command here' | iconv -t utf-16le | base64 -w 0
