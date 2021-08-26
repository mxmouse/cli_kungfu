**Cyber Aegis workshop

# ⚡ Linux - Intro ⚡
![external-content duckduckgo com](https://media.giphy.com/media/Bak719jJB7mko/giphy.gif)
## Summary
* [History](#history)
  * [GNU/Linux](#history-of-gnu-linux)
  * [Root](#history-of-root)
  * [Shell](#history-of-the-shell)
* [What is the command line?](#what-is-command-line)
* [User groups and Root](#user-groups-and-root)

## HISTORY
---
### History of gnu linux
Before we jump into the history of root, I wanted to highlight the impressive minds that manifested the GNU/Linux operating system and why GNU/Linux is a very important fixture for technoolgists and end users. Learning GNU/Linux is a step towards technological empowerment. 

First, there is a some debate around what to call "Linux" vs GNU/Linux. "GNU/Linux" is technically the correct term because Linux is only the kernel of the GNU system -- albeit an important component.  Richard Stallman began developing GNU in 1983. He foresaw a need for users to have "free software". In fact, he believes that technologist, or "programmers, need to share, redistribute study and improve the software we write"
If you want to read Stallman's [philosophy](https://www.gnu.org/philosophy/shouldbefree.en.html) (really a manifesto) behind GNU, you won't be disappointed. TL;DR - GNU is based on the "Free Software" principle, in that it "respects user' freedom...the development of GNU made it possible to use a computer without software that would trample your freedom"

Something to note is that "Free software" is different to "open source". If you want to read about the difference go [here](https://www.gnu.org/philosophy/open-source-misses-the-point.html) 

The Linux kernel was created in 1991 by Linus Torvaids as a personal project with the goal to create a free operating system kernel. 

[Linux Distribution Timeline](https://upload.wikimedia.org/wikipedia/commons/thumb/1/1b/Linux_Distribution_Timeline.svg/3020px-Linux_Distribution_Timeline.svg.png)

### History of root
- Root is omnipotent with unrestricted access to all commands, files, directories and resources
- Root is the actual name of an admin account. 'sudo' is a command which allows ordinary users to perform admin tasks

### History of the Shell
Shells are pivotal to the Linux user. There are different shells within Linux to accomplish tasks. Each shell has inuqie properties. Hence, there are many intances where oen shell is better than the other for specific requirements

This is what made it the default shell for Solaris OS. It is also used as the default shell for all Solaris system administration scripts. Start reading about shell scripting here.

#### WHAT IS A SHELL AND WHY DO WE NEED THEM? 

(Take from https://www.journaldev.com/39194/different-types-of-shells-in-linux)
Whenever a user logs in to the sytem or opens a console window, the kernel runs a new shell instance. The kernel is the heart of any operating system. 

It is responsible for the control management, and execution of processes, and to ensure proper utilization of system resources. 

A shell is a program that acts an interface between a user and the kernel. It allows a user to give commands to the kernel and receive responses from it. Through a shell, we can execute programs and utilities on the kernel. Hence, as its core, a shell is a pogram used to execute other programs on our system

Being able to interact with the kernel makes shells a powerful tool. Without the ability to interact with the kernel, a user cannot access the utilities offered by their machines operating system. 

Let's understand the different types of shell available for the Linux environment. 

#### THE BOURNE SHELL (sh)

Developed at AT&T Bell Labs by Steve Bourne, the Bourne shell is regarded as the first UNIX shell ever. It is denoted as sh. It gained popularity due to its compact nature and high speeds of operation.

However, the Bourne shell has some major drawbacks.

- It doesn’t have in-built functionality to handle logical and arithmetic operations.
- Also, unlike most different types of shells in Linux, the Bourne shell cannot recall previously used commands.
- It also lacks comprehensive features to offer a proper interactive use.

The complete path-name for the Bourne shell is /bin/sh and /sbin/sh. By default, it uses the prompt # for the root user and $ for the non-root users.

#### THE GNU BOURNE-AGAIN SHELL (bash)

More popularly known as the Bash shell, the GNU Bourne-Again shell was designed to be compatible with the Bourne shell. It incorporates useful features from different types of shells in Linux such as Korn shell and C shell.

It allows us to automatically recall previously used commands and edit them with help of arrow keys, unlike the Bourne shell.

The complete path-name for the GNU Bourne-Again shell is /bin/bash. By default, it uses the prompt bash-VersionNumber# for the root user and bash-VersionNumber$ for the non-root users.

#### THE C SHELL (csh)

The C shell was created at the University of California by Bill Joy. It is denoted as csh. It was developed to include useful programming features like in-built support for arithmetic operations and a syntax similar to the C programming language.

Further, it incorporated command history which was missing in different types of shells in Linux like the Bourne shell. Another prominent feature of a C shell is “aliases”.

The complete path-name for the C shell is /bin/csh. By default, it uses the prompt hostname# for the root user and hostname% for the non-root users.

#### THE KORN SHELL (ksh)

The Korn shell was developed at AT&T Bell Labs by David Korn, to improve the Bourne shell. It is denoted as ksh. The Korn shell is essentially a superset of the Bourne shell.

Besides supporting everything that would be supported by the Bourne shell, it provides users with new functionalities. It allows in-built support for arithmetic operations while offereing interactive features which are similar to the C shell.

The Korn shell runs scripts made for the Bourne shell, while offering string, array and function manipulation similar to the C programming language. It also supports scripts which were written for the C shell. Further, it is faster than most different types of shells in Linux, including the C shell.

The complete path-name for the Korn shell is /bin/ksh. By default, it uses the prompt # for the root user and $ for the non-root users.

#### THE Z SHELL (zsh)

The Z Shell or zsh is a sh shell extension with tons of improvements for customization. If you want a modern shell that has all the features a much more, the zsh shell is what you’re looking for.

Some noteworthy features of the z shell include:

-Generate filenames based on given conditions
-Plugins and theming support
-Index of built-in functions
-Command completion
-and many more…

| Shell | Complete path-name | Prompt for root user| Prompt for non root user |
|--------------|-------------------|---------------------|-------------------------|
|Bourne shell (sh) | /bin/sh and /sbin/sh | # | $ |
|GNU Bourne-Again shell (bash)| /bin/bash | bash-VersionNumber#|bash-VersionNumber$|
|C shell (csh) | /bin/csh | #| % |
|Korn shell (ksh) | /bin/ksh| #| $|
|Z Shell (zsh) | /bin/zsh | <hostname># | <hostname>% |

## What is the command line?
A user interface that's navigated by typing commands at prompts, instead of using a mouse. (I stole this definition from duck duck go)

## User Groups and Root
To create a secure environment in GNU/Linux, you need to learn about user groups. 

#### File Permissions Review
File permissions relates to who owns a file therefore who can access specific information within an organization
1. User: the owner of the file (person who created the file)
2. Group: The group can contain multiple users, therefore possessing the same permissions. 
3. Other: any person has access to that file, that person has neither created the file, nor are they in any group which has access to that file.

- By typing the following in a shell: 
   ```powershell
   ls -l
   ```

- We will return the file permissions which might look something like this: 
    ```powershell
    (ɔ◔‿◔ )ɔ ♥ $ ls -l
    total 0
    -rw-r--r-- 1 hellcat hellcat 0 Aug 24 22:46 file.txt
    ```

The above characters mean the following: 
* 'r' = read
* 'w' = write
* 'x' = execute
* '-' = no permission

![external-content duckduckgo com](https://www.section.io/engineering-education/user-groups-and-permissions-linux/2.png)

The empty first part means that it is a file. If it were a directory (or folder) then it would marked with a "d" like so: 

- Directory example
   ```powershell
   drwxrwxr-x 2 hellcat hellcat  4096 Aug 21 23:16 enumeration 
   ```
The second part means that the user "home" has read and write permissions but she does not have the ability to execute. The group and others only have read permissions.

To grant write permissions to other users run the following: 

- Changing file permissions: 
   ```powershell
   chmod o+w file.txt
   ```
This will return the followin perms ```-rw-r--rw-```

"o" refers to others, "g" for the group, "u" for the user and "a" for all. 

- If you want to add execute permission to the user, run the following command:
   ```powershell
   chmod u+x file.txt
   ```

The permissions will now be ```-rwxr--rw-```

- If you want to remove the permission, you can use the same method but with “-” instead of “+”.
   ```powershell
   chmod ux file.txt
   ```
Now the permissions will be: ```-rw-r--rw-.```

Finally, you can use the Symbolic Mode to modiy permissions: 

| Number | Permission |
|------|----------|
| 0 | No permission |
| 1 | Execute |
| 2 | Write |
| 3 | Execute and Write |
| 4 | Read |
| 5 | Read and Execute |
| 6 | Read and Write |
| 7 | Read, Write and Execute |

- For example ```chmod 777``` will give every permission for all with: 
   ```powershell
   chmod 777 file.txt
   ```
Which will return these permissions: ```-rwxrwxrwx```

- ```chmod 765``` will remove the execute permission from the group and write from other:
  ```powershell
   chmod 765 file.txt
   ```
This will return these permissiosn: ```-rwxrw-r-x```

#### passwd
`/etc/passwd` is a plain text-based database that contains information for all user accounts on the system. It is owned by root and has 644 permissions . The file can only be modified by root or users with sudo privileges and readable by all system users.



#### What do you use passwd for? 
* To see senstive files
* As a regular user should only ever be able to see ```-rw-r--r--```
* Does not contain any passwords
* Allows us to identify what users are on the machine
* "back in the day", passwords used to be stored in the passwd file but now they are stored in the shadow file
* The "x" marks where the password holder

#### How to see it?
- To get started:
  ```powershell
   cat /etc/passwd
   ```
You should see something like this: 
![external-content duckduckgo com](https://media.geeksforgeeks.org/wp-content/uploads/20210718172639/ectfile.png)

The user information contains seven fields and each field is separated by the colon ( : )symbol. Each entry in the /etc/passwd file looks like this:

```gfg:x:1000:1000:main user:/home/gfg:/usr/bin/zsh```
- 
Broken down even further:
 
gfg: | x: | 1000: | 1000: | main user: | /home/gfg: | /usr/bin/zsh
:---------: | :---------: | :-----------: | :--------------: | :--------------------: | :---------------: | :--------------: 
1. Username | 2. Password | 3. UserID(UID | 4. GroupID(GID) | 5. User ID Info (GECOS) | 6. Home Directory | 7. Login shell |

1. Username: This field stores the usernames which are used while login into the system. The length of this field is between 1 and 32 characters.
2. Password: This field store the password of the user. The x character indicates the password is stored in /etc/shadow file in the encrypted format. We can use the passwd command to update this field.
3. User ID(UID): User identifier is the number assigned to each user by the operating system to refer the users. The 0 UID is reserved for the root user. And 1-99 UID are reserved for other predefined accounts. And 100-999 are reserved by the system for administrative and system accounts/groups.
4. Group ID(GID): Group identifier is the number indicating the primary group of users. Most of the time it is the same as the UID.
5. User ID Info (GECOS): This is a comment field. This field contains information like the user phone number, address, or full name of the user. This field is used by the finger command to get information about the user.
6. Home directory: This field contains the absolute path of the user’s home directory. By default, the users are created under the /home directory. If this file is empty, then the home directory of that user will be /
7. Login shell: This field store the absolute path of the user shell. This shell is started when the user is log in to the system.


#### Handy Commands
-  ```cat /etc/passwd | cut -d : -f 1```
cuts all the junk out
cut "delimieter" which is ":" and "field" 1


## shadow
### What is a shadow file? 

###looking at /etc/passwd and /etc/shadow

    take the contents of these files and put them into a file called "passwd" and "shadow"
    Run: unshadow PASSWORD-FILE SHADOW-FILE
        -copy the contents of the file to a new file
        -save the root and user information
        -need identify the hashing types
        -go to google and look up "hashcat has types"
        -https://hashcat.net/wiki/doku.php?id=example_hashes
    Put through the haschat text


## REFERENCES
---
* [Richard Stallmans on why software should be free](https://www.gnu.org/philosophy/shouldbefree.en.html)
* [Different types of shells in linux](https://www.journaldev.com/39194/different-types-of-shells-in-linux)
* [History of linux](https://en.wikipedia.org/wiki/History_of_Linux)
* [User Groups and Permissions in Linux](https://www.section.io/engineering-education/user-groups-and-permissions-linux/)
* [Etc Passwd File](https://linuxize.com/post/etc-passwd-file/)
* [Understanding the etc passwd file](https://www.geeksforgeeks.org/understanding-the-etc-passwd-file/)**