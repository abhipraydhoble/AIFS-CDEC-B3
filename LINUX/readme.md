
## Operating System:
- An operating system (OS) is a system software that manages computer hardware and software resources 
- and acts as an intermediary between the user and the hardware.


## Distributions of Linux
- redhat
- dabian
- fedora
- ubuntu
- amazon linux
- kali linux
- mint
- suse

    
---



## Linux Basic Commands:

**switch to root user**
````
sudo -i
````
- exit the terminal
```bash
exit
```
**shows present working dir**
````
pwd
````
**display os informaton**
````
cat /etc/os-release
````

**display memory information**
````
free -h
````
**display disk information**
````
df -h
````

**list files and dir's**
````
ls
````

**change directory**
````
cd <dirname>
````
**back to previous dir**
````
cd ..
````

---

## Directory  Structure in  Linux:

-In Linux directory structure   “/”  (slash) is main directory
- All other directories comes under “/” directory.




1. / - The main folder.


2. /bin - Basic commands everyone uses (e.g., ls, cp).


3. /sbin - Commands for system admins (e.g., reboot).


4. /usr - Programs and tools for users.


5. /var - Stores changing files like logs.


6. /tmp - Temporary files that auto-delete.


7. /etc - System settings and configuration files.


8. /dev - Files that connect to hardware (e.g., USB).


9. /proc - Info about running programs and the system.


10. /sys - Details about hardware and devices.


11. /lib - Helper files for programs to run.


12. /boot - Files needed to start the computer.


13. /home - home dir of local user.


14. /opt - Extra programs you install.


15. /root - home dir of root user


16. /media - Automatically mounted drives (e.g., USB).


17. /mnt - Manually mounted drives.


18. /srv - Files for server programs (e.g., websites).


19. /run - Temporary system files from this boot.
---
# Linux Directory and File Creation


## Creating Files
````
touch example.txt
````
- touch example.txt → Creates empty file example.txt 


- echo "Hello World" > index.html → Creates a file index.html and writes Hello World into it.
````
echo "Hello World" > index.html
````

**Displaying File Content**
````
cat index.html
````
---

###  Creating Directories
```sh
mkdir pune
```


### Remove files/Dir

````
rm -rvf pune
````
- r recursive
- v verbose
- f forcefully

### Copy file to another file and dir
````
cp file1.txt  file2.txt
````

````
mv demo.txt Documents/
````

### Moving a File to Another Directory
```sh
mv index.html pune/
```


###  Renaming a File
```sh
mv samantha.txt samartha.txt
```
- Renames `samantha.txt` to `samartha.txt` 


---
#  nano editor

### create file with nano editor
````
nano example.txt
````

- to save file press **cntrl + x** then **y** and **enter**


# Vi / Vim Editor

Modes of vi/vim editor:
1. **Command Mode(default)**
2. **Insert Mode**
3. **Execution Mode**
4. **Visual Mode**

### Note:
Press `Esc` to exit from any mode.

---

## 1. Command Mode: (Default Mode)
In **Command Mode**, you can perform operations like deleting, copying, and pasting text, as well as navigating and editing the file. 

### Common Commands:
- dd  Delete current line
- G or L  Move cursor to the end of the file


---

## 2. Insert Mode

To enter **Insert Mode**, use the following commands:

- i  Insert text at the current cursor position

---

## 3. Execution Mode


- :q!  Quit without saving, forcefully
- :wq  Save and quit
- :x  Save and quit


---

