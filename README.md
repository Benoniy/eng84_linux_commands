## Linux:  
* `man cmd` - Manual of the command
* `apt (install | remove)` - Package manager  
* `mkdir` - Make folder  
* `ls (-a)` - list files, -a shows all files  
* `nano` - text editor  
* `touch` - makefile  
* `cd` .. - up a dir  
* `pwd`  - print working directory  
* `mv` - move also used to rename  
* `cp` - copy  
* `rm` - remove  
* `ll` - check permissions  
* `chmod (+rwx | -rwx)` - change permissions  
  * `+ | -` - add or remove permission  
  * `r` - read permission  
  * `w` - write permission  
  * `x` - execute permission  
  * `777` - read, write and execute for everyone  
  * `400` - same as 777 but only for the issuing user  
  * `600` - same as 777 but only for the file owner and restricts all others  
  
* `top` - task manager  
* `kill pid` - Kills a process based on its pid  
* `sudo systemctl (status | start | stop | restart)` - Manage background services  
* Wildcards:  
  * `*` - All files  
  * `.` - Current folder  
  * `..` - Up one folder  
  
* `head` - prints first 10 lines of a file  
* `tail` - prints last 10 lines of a file  
* `sort` - sorts information in a file  
* `nl` - prints a file with numbered lines  
* `wc` - print out a word count  
* `cmd 1 | cmd 2` - Use command 1 and use that output as input for command 2  
* `cmd > file` - redirect output into a file and overwrite the contents  
* `cmd >> file` - redirect output into a file and append it to the end  


* Transfer files to the instance:  
  ```
  scp -ri ~/.ssh/.pem /file_to_transfer ubuntu@<ip>:~/location
  ```


* Fix DOS conversion error:
  ```
  wget "http://ftp.de.debian.org/debian/pool/main/d/dos2unix/dos2unix_6.0.4-1_amd64.deb"
  sudo dpkg -i dos2unix_6.0.4-1_amd64.deb
  ```


* Proxy SSH into our private network:  
  ```
  ssh -i ~/.ssh/local.pem -o ProxyCommand="ssh -i ~/.ssh/local.pem -W %h:%p ubuntu@app_ip" ubuntu@db_private_ip
  ```
  
