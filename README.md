

# /Devops/ [![Awesome](https://cdn.jsdelivr.net/gh/sindresorhus/awesome@d7305f38d29fed78fa85652e3a63e154dd8e8829/media/badge.svg)](https://github.com/sindresorhus/awesome#readme) <img src="https://raw.githubusercontent.com/MartinHeinz/MartinHeinz/master/wave.gif" width="30px" height="30px" />


| Subject | Image Link | Description  |
| :---: | :---: | :---: |
| Interview Questions | [![linux](https://encrypted-tbn0.gstatic.com/images?q=tbn:ANd9GcRXig82Iv8wtBUnwtsKl7vXi1nVFRk9Qtrlog&s)](https://github.com/M0G3H/Devops#interview-questions) | Click in image to go |
| Usefull Command | [![linux](https://cdn-icons-png.freepik.com/256/15210/15210895.png?semt=ais_hybrid)](https://github.com/M0G3H/Devops#usefull-command) | Click in image to go |




# Interview Questions
## Simple Linux Questions

<details>
<summary>What is the name and the UID of the administrator user?</summary>
<br>
Name: root, UID: 0
</details>

<details>
<summary>How to list all files, including hidden ones, in a directory?</summary>
<br>
`ls -a`
</details>

<details>
<summary>What is the Unix/Linux command to remove a directory and its contents?</summary>
<br>
`rm -r directoryname`
</details>

<details>
<summary>Which command will show you free/used memory? Does free memory exist on Linux?</summary>
<br>
`free -h`. Linux uses all available memory for caching, so "free" memory is minimal by design.
</details>

<details>
<summary>How to search for the string "my konfu is the best" in files of a directory recursively?</summary>
<br>
`grep -r "my konfu is the best" /path/to/directory`
</details>

<details>
<summary>How to connect to a remote server or what is SSH?</summary>
<br>
`ssh username@hostname`. SSH (Secure Shell) is a protocol for secure remote login.
</details>

<details>
<summary>How to get all environment variables and how can you use them?</summary>
<br>
`printenv` or `env`. They can be accessed in scripts/shell as `$VARNAME`.
</details>

<details>
<summary>I get "command not found" when I run `ifconfig -a`. What can be wrong?</summary>
<br>
The `net-tools` package isn't installed. Use `ip a` instead (modern replacement).
</details>

<details>
<summary>What happens if I type TAB-TAB?</summary>
<br>
It triggers shell autocomplete, showing all possible completions for the current command.
</details>

<details>
<summary>What command will show the available disk space on the Unix/Linux system?</summary>
<br>
`df -h`
</details>

<details>
<summary>What commands do you know that can be used to check DNS records?</summary>
<br>
`dig`, `nslookup`, `host`
</details>

<details>
<summary>What Unix/Linux commands will alter a files ownership, files permissions?</summary>
<br>
`chown` (ownership), `chmod` (permissions)
</details>

<details>
<summary>What does `chmod +x FILENAME` do?</summary>
<br>
Adds execute permission to the file for all users.
</details>

<details>
<summary>What does the permission 0750 on a file mean?</summary>
<br>
Owner: read/write/execute (7), group: read/execute (5), others: no permissions (0).
</details>

<details>
<summary>What does the permission 0750 on a directory mean?</summary>
<br>
Same as files but execute means "search/traverse" permission for directories.
</details>

<details>
<summary>How to add a new system user without login permissions?</summary>
<br>
`useradd -s /sbin/nologin username`
</details>

<details>
<summary>How to add/remove a group from a user?</summary>
<br>
Add: `usermod -aG groupname username`, Remove: `gpasswd -d username groupname`
</details>

<details>
<summary>What is a bash alias?</summary>
<br>
A shortcut for commands, defined in `~/.bashrc` (e.g., `alias ll='ls -la'`).
</details>

<details>
<summary>How do you set the mail address of the root/a user?</summary>
<br>
Edit `/etc/aliases` for root, or user's `~/.forward` file.
</details>

<details>
<summary>What does CTRL-c do?</summary>
<br>
Sends SIGINT, terminating the foreground process.
</details>

<details>
<summary>What does CTRL-d do?</summary>
<br>
Sends EOF (End Of File), often exiting the shell or program.
</details>

<details>
<summary>What does CTRL-z do?</summary>
<br>
Sends SIGTSTP, suspending the foreground process.
</details>

<details>
<summary>What is in /etc/services?</summary>
<br>
A list of network services and their associated port numbers.
</details>

<details>
<summary>How to redirect STDOUT and STDERR in bash?</summary>
<br>
`command > /dev/null 2>&1` (redirects both to null)
</details>

<details>
<summary>What is the difference between UNIX and Linux?</summary>
<br>
Linux is a UNIX-like kernel; UNIX refers to original AT&T OS and certified variants.
</details>

<details>
<summary>What is the difference between Telnet and SSH?</summary>
<br>
SSH is encrypted, Telnet sends data in plaintext (insecure).
</details>

<details>
<summary>Explain the three load averages and what do they indicate.</summary>
<br>
1/5/15 minute system load averages (CPU demand). Check with `uptime` or `top`.
</details>

<details>
<summary>Can you name a lower-case letter that is not a valid option for GNU `ls`?</summary>
<br>
`-h` is valid (human-readable), but `-z` isn't a standard `ls` option.
</details>

<details>
<summary>What is a Linux kernel module?</summary>
<br>
Loadable kernel component that adds functionality without rebooting.
</details>

<details>
<summary>Walk me through the steps in booting into single user mode.</summary>
<br>
1. Edit GRUB (add `single` or `1` to kernel line) 2. Boot to root shell.
</details>

<details>
<summary>Walk me through troubleshooting a 404 error.</summary>
<br>
1. Check URL 2. Verify file exists 3. Check permissions 4. Review web server logs.
</details>

<details>
<summary>What is ICMP protocol?</summary>
<br>
Internet Control Message Protocol, used for diagnostics (ping, traceroute).
</details>

## Medium Linux Questions

<details>
<summary>What does `tee` do?</summary>
<br>
Reads stdin and writes to both stdout and files (`command | tee file.txt`).
</details>

<details>
<summary>What does `awk` do?</summary>
<br>
Pattern scanning/text processing language (`awk '{print $1}' file`).
</details>

<details>
<summary>What does `tr` do?</summary>
<br>
Translates/deletes characters (`tr 'a-z' 'A-Z'` for uppercase).
</details>

<details>
<summary>What does `&` after a command do?</summary>
<br>
Runs command in background (`command &`).
</details>

<details>
<summary>What is Virtual Memory?</summary>
<br>
Memory abstraction using RAM + disk swap space to extend available memory.
</details>

<details>
<summary>What is swap and what is it used for?</summary>
<br>
Disk space used when RAM is full (emergency memory).
</details>

<details>
<summary>What is an A record?</summary>
<br>
DNS record mapping hostname to IPv4 address.
</details>

<details>
<summary>What is the sticky bit?</summary>
<br>
Directory permission restricting file deletion to owner (e.g., `/tmp`).
</details>

<details>
<summary>What is the difference between hardlinks and symlinks?</summary>
<br>
Hardlink: direct inode reference. Symlink: pointer to filename (breaks if source removed).
</details>

<details>
<summary>What is an inode?</summary>
<br>
Filesystem metadata structure storing file attributes (except name/path).
</details>

## Networking Questions

<details>
<summary>What is localhost?</summary>
<br>
Loopback interface (127.0.0.1). Ping fails if network stack is broken.
</details>

<details>
<summary>What is the similarity between ping & traceroute?</summary>
<br>
Both use ICMP. Traceroute uses TTL expiry to discover hops.
</details>

<details>
<summary>Command to show open ports?</summary>
<br>
`ss -tulnp` or `netstat -tulnp` (older).
</details>

<details>
<summary>Is 300.168.0.123 valid?</summary>
<br>
No, IPv4 octets max at 255.
</details>

<details>
<summary>What are private IP ranges?</summary>
<br>
10.0.0.0/8, 172.16.0.0/12, 192.168.0.0/16 (RFC 1918).
</details>

## MySQL Questions

<details>
<summary>How do you create a user?</summary>
<br>
`CREATE USER 'username'@'host' IDENTIFIED BY 'password';`
</details>

<details>
<summary>Difference between LEFT and RIGHT join?</summary>
<br>
LEFT: all rows from left table. RIGHT: all rows from right table.
</details>

## DevOps Questions

<details>
<summary>What is GIT?</summary>
<br>
Use Control + Shift + m to toggle the tab key moving focus. Alternatively, use esc then tab to move to the next interactive element on the page.
No file chosen
Attach files by dragging & dropping, selecting or pasting them.
Editing Devops/README.md at main · M0G3H/Devops

PowerUP kit

Distributed version control system for tracking code changes.
</details>

<details>
<summary>What is the difference between Containers and VMs?</summary>
<br>
Containers share host OS kernel, VMs emulate full hardware with separate OS.
</details>

<details>
<summary>What is continuous delivery?</summary>
<br>
Automated process to deploy code changes reliably and frequently.
</details>

# Usefull Command

## linux

<details>
<summary>enables IP forwarding</summary>
<br>
sysctl -w net.ipv4.ip_forward=1
</details>

<details>
<summary>delete network interface</summary>
<br>
ip link delete "a2"
</details>

<details>
<summary>install openssh</summary>
<br>
sudo apt update  
sudo apt install openssh-client
</details>

<details>
<summary>NC</summary>
<br>
nc -ul 200  
nc -u 10.0.0.1 200
</details>

<details>
<summary>error: externally-managed-environment</summary>
<br>
python3 -m venv venv  
source venv/bin/activate  
pip install -r requirements.txt
</details>

<details>
<summary>make .deb package</summary>
<br>
dpkg-deb --build mypackage
</details>

<details>
<summary>ova to ovf</summary>
<br>
tar -xvf vm-export.ova
</details>

<details>
<summary>making .deb package again</summary>
<br>
dpkg-deb --build package.deb
</details>

<details>
<summary>restart networking</summary>
<br>
systemctl restart systemd-networkd
</details>

<details>
<summary>find and kill process</summary>
<br>
sudo lsof -i :400  
kill -9 1979
</details>

<details>
<summary>check current OS version</summary>
<br>
lsb_release -a
</details>

<details>
<summary>make a screen</summary>
<br>
screen -ls  
screen -r "name"  
screen -S "name"  
screen -D "name"
</details>

<details>
<summary>make a virtual network card</summary>
<br>
sudo ./netns.sh  
ip netns  
ip netns exec ns5 bash  
ip netns id
</details>

<details>
<summary>copy with scp</summary>
<br>
scp /path/to/local/file username@ip:/path/to/remote/directory
</details>

## docker

<details>
<summary>enter container</summary>
<br>
docker exec -it --privileged "docker name" /bin/bash
</details>

<details>
<summary>clone container</summary>
<br>
docker commit &lt;container_name_or_id&gt; &lt;new_image_name&gt;
</details>

<details>
<summary>view containers</summary>
<br>
docker ps -a
</details>

<details>
<summary>start container</summary>
<br>
docker start c1
</details>

<details>
<summary>stop container</summary>
<br>
docker stop c1
</details>

<details>
<summary>delete container</summary>
<br>
docker rm -f c10
</details>

<details>
<summary>find images</summary>
<br>
docker images
</details>

<details>
<summary>create container</summary>
<br>
docker run -i -t -d --privileged --network=host --name c12 client
</details>

<details>
<summary>create multiple containers</summary>
<br>
for i in {6..10}; do docker run -i -t -d --privileged --network=host --name "c$i" client; done
</details>

<details>
<summary>rename container</summary>
<br>
docker rename vbox c3
</details>

<details>
<summary>copy files into container</summary>
<br>
docker cp /home/admin/tools c1:/home/ubuntu/client
</details>

<details>
<summary>get container IP</summary>
<br>
docker inspect -f '{{range .NetworkSettings.Networks}}{{.IPAddress}}{{end}}' server
</details>

<details>
<summary>save docker image</summary>
<br>
docker save -o client-full.tar c1
</details>

<details>
<summary>load docker image</summary>
<br>
docker load -i client-full.tar
</details>

## iperf

<details>
<summary>server</summary>
<br>
iperf -s -P 10
</details>

<details>
<summary>client</summary>
<br>
iperf -c 192.168.1.146
</details>

## gitlab

<details>
<summary>first-time clone</summary>
<br>
git clone http://example.com/test
</details>

<details>
<summary>add and push</summary>
<br>
git add .  
git commit -m "detail"  
git push
</details>

## andriod

<details>
<summary>get shell</summary>
<br>
adb shell
</details>

<details>
<summary>root access</summary>
<br>
adb root
</details>

<details>
<summary>push file to android</summary>
<br>
adb push /path/to/file /destination/directory
</details>

<details>
<summary>pull file from android</summary>
<br>
adb pull /path/to/file /destination/directory
</details>

## make service in linux

<details>
<summary>write shell script</summary>
<br>
sudo nano /path/to/file/service.sh
</details>

<details>
<summary>make it executable</summary>
<br>
sudo chmod +x /path/to/file/service.sh
</details>

<details>
<summary>create systemd service</summary>
<br>
sudo nano /etc/systemd/system/service.service
</details>

<details>
<summary>service file content</summary>
<br>
[Unit]  
Description=...  
After=network.target  

[Service]  
Type=simple  
ExecStart=/usr/local/bin/service.sh  
Restart=on-failure  
User=root  

[Install]  
WantedBy=multi-user.target
</details>

<details>
<summary>enable and start service</summary>
<br>
sudo systemctl daemon-reload  
sudo systemctl enable service.service  
sudo systemctl start service.service  
sudo systemctl status service.service
</details>

