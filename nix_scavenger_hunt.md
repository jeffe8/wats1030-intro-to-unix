# *nix Scavenger Hunt

Complete the following challenges using the command-line interface on your favorite
Unix or Linux operating system. You are welcome and encouraged to consult any
additional documentation online or in books.

Please add your answers/responses/text pastes to the document after each prompt.

Note: For some of the challenges you will need to reference files included with
this repository, so you will need to fork the repo into your own Github account
and then clone it to your development environment.

## The Challenges

### Navigating the Filesystem

* Get an idea of where you are in the operating system. Use the `pwd` command to find your "path to working directory"--your current location in the filesystem of your devbox. *Paste the output of the `pwd` command here:*  /home/cabox/workspace
* Discover more about this filesystem. Use `ls` (the "list" command)to see what is in this directory. *What directories and files do you see when you run `ls`?* LICENSE  README.md  challenge_files  nix_scavenger_hunt.md  nix_scavenger_hunt_stretch.md  super_scavengers.md

* You can use *options* to modify how a command runs. Try using `ls -alh` to see the contents of your current directory. *How are the results different when you use the `-alh` options?* total 40K
drwxrwxr-x  4 cabox cabox 4.0K Apr 14 18:23 .
drwxr-xr-x 11 cabox cabox 4.0K Apr 14 18:23 ..
drwxrwxr-x  8 cabox cabox 4.0K Apr 14 18:23 .git
-rw-rw-r--  1 cabox cabox 1.1K Apr 14 18:23 LICENSE
-rw-rw-r--  1 cabox cabox 2.7K Apr 14 18:23 README.md
drwxrwxr-x  7 cabox cabox 4.0K Apr 14 18:23 challenge_files
-rw-rw-r--  1 cabox cabox 5.4K Apr 14 18:23 nix_scavenger_hunt.md
-rw-rw-r--  1 cabox cabox  317 Apr 14 18:23 nix_scavenger_hunt_stretch.md
-rw-rw-r--  1 cabox cabox  191 Apr 14 18:23 super_scavengers.md


* The `man` ("manual") command tells you more about how any given command works. (*WARNING:* CodeAnywhere does not support the man command. You can click the following link to complete this task: http://man.he.net/). Run `man` to see instructions about how to use `man`. Then use `man` to learn what the `a`, `l`, and `h` options mean when used with the `ls` command. *Write down what those options do?* -a: find all matching entries; -c: do use cat file; -d: print gobs of debugging information; -D: as for -d, but also display the pages; -l: list man functions; -h: print this help message; 

* Commands can also take *arguments*, which are usually the names of files or locations that you want the command to work with. Try running `ls /` to see what files are in the *root* directory of the filesystem. *What files and directories do you see listed?*
bin  boot  dev  etc  fastboot  home  lib  lib64  media  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var

* A Unix filesystem has a few special shortcuts to refer to specific locations. `/` indicates the *root* of the filesystem, meaning the top-most directory in the filesystem hierarchy. Use the `cd` ("change directory") command to move to the root directory. (Hint: Use `man` to look up the `cd` command if you have any issues) *Then run `pwd` and paste the output here:*  /home/cabox


* Another special shortcut in Unix is the `~` location. This indicates the *user root* directory, meaning the top-most directory in the hierarchy that comes below your user account. Use `cd` to move to `~`. *Run `pwd` and paste the response here:*  /home/cabox


* Change directory into the `challenge_files` directory. Use `ls` to find only the files with a `.demo` pattern. *How many files do you find?* 3 files: 2015_special_stuff.demo; cloaked-wookie.demo; scooter-double-mamba.demo

* Use the `cd` command to move "up" one directory. *Where are you in the filesystem now?*  /home/cabox

* Press the up arrow on your keyboard. *What just happened?* Repeated the pwd command!

* Press the up arrow a few more times. *What do you see?* Aw sweet! It is showing my old commands that I have input previously!!

* Run the `history` command. *What do you see?*  Shows all the commands used throughout this session

### Observing the System

* Discover what account you are logged into using the `whoami` command. *What username are you currently using?*  cabox

* Discover who else is on your system with the `who` command. *Are any other users using your system? If so, list them here:*  cabox    pts/0        Apr 14 18:39 (52.161.27.120)

* How long has your system been running? Use `uptime` to see, and *paste the result here:*   18:53:47 up 31 min,  1 user,  load average: 0.00, 0.00, 0.00

* Run `ps aux` and review the results. (Hint: Use `man` to learn more about the `ps` command and options.) *How do you interpret what you see here?*  
USER       PID %CPU %MEM    VSZ   RSS TTY      STAT START   TIME COMMAND
root         1  0.0  0.4  33196  2556 ?        Ss   18:22   0:00 init
root         2  0.0  0.0      0     0 ?        S    18:22   0:00 [kthreadd/163461]
root         3  0.0  0.0      0     0 ?        S    18:22   0:00 [khelper/1634618]
root       153  0.0  0.1  19428   824 ?        S    18:22   0:00 upstart-udev-bridge --daemon
root       177  0.0  0.2  49216  1408 ?        Ss   18:22   0:00 /lib/systemd/systemd-udevd --daemon
syslog     321  0.0  0.2 184188  1444 ?        Ssl  18:22   0:00 rsyslogd
root       403  0.0  0.5  61316  3076 ?        Ss   18:22   0:00 /usr/sbin/sshd -D
root       449  0.0  0.1  15608  1040 ?        S    18:22   0:00 upstart-socket-bridge --daemon
root       454  0.0  0.1  15492   860 ?        S    18:22   0:00 upstart-file-bridge --daemon
root       461  0.0  0.5  71272  3116 ?        Ss   18:22   0:00 /usr/sbin/apache2 -k start
root       528  0.0  0.1  12740   852 tty1     Ss+  18:22   0:00 /sbin/getty 38400 console
root       530  0.0  0.1  12740   860 tty2     Ss+  18:22   0:00 /sbin/getty 38400 tty2
www-data   560  0.0  0.4 415724  2444 ?        Sl   18:22   0:00 /usr/sbin/apache2 -k start
www-data   561  0.0  0.4 415724  2448 ?        Sl   18:22   0:00 /usr/sbin/apache2 -k start
root       639  0.0  0.6  63876  3328 ?        Ss   18:23   0:00 sshd: cabox [priv]
cabox      641  0.0  0.2  64168  1516 ?        S    18:23   0:00 sshd: cabox@notty
cabox      642  0.0  0.1  12780   976 ?        Ss   18:23   0:00 /usr/lib/openssh/sftp-server
root       643  0.0  0.6  63876  3476 ?        Ss   18:39   0:00 sshd: cabox [priv]
cabox      645  0.0  0.2  63876  1464 ?        S    18:39   0:00 sshd: cabox@pts/0
cabox      646  0.0  0.8  20560  4460 pts/0    Ss   18:39   0:00 -bash
cabox      858  0.0  0.2  15520  1144 pts/0    R+   18:54   0:00 ps aux

* Run `top` and review the results. (Hint: You may need to use `ctrl-c` to get out of this app.) *How do you interpret what you see here?* pushes code to the top of the screen - cleans up the viewer


### Finding and Viewing Files

* Make sure you are in the `challenge_files` directory. Use the `*` wildcard to find all the files that have the word "credit" in the filename. *How many files did you find?* It looks like only one file is showing - -bash: credit_cards.txt: command not found - But it also looks like the command is incorrect.  I have tried looking at the resouces and the only one showing is credit* for the command.  Nothing else worked


* Use the `more` command to view one of the `credit_cards` files you just discovered. (Hint: Type `q` to quit viewing the file. Press the `spacebar` to page down. Use your keyboard arrows to move up/down.) *What is the date in the file you have viewed?*  01-15-2015

* Use the `find` command to search for files more effectively. Search the sub-directories under `challenge_files` to find the location of the file named `modi_laboriosam.txt`. *Where is that file located?* ./tmp/modi_laboriosam.txt

* Use the `grep` command to search for text within a file. Use `grep` on all the `.user` files in `challenge_files` to find which files contain "WA" (the abbreviation for Washington state). *How many files did you find?* 
Lissie-Strosin.user:Jewessfurt, WA 00816-7241
Britt-Erdman.user:O'Harachester, WA 37261

* Use the `-r` option of `grep` to *recursively* find the text "Waldo" hidden in a file somewhere under the `challenge_files` directory. *Paste the result showing the file and line where the word "Waldo" shows up.*  challenge_files/serial-numbers/eaque_molestiae.txt:Ut est maiores quia autem. Nisi modi Waldo sed corporis sit explicabo ut est. Et est placeat ea sunt sunt consectetur sunt incidunt. Explicabo vel esse blanditiis dolorem culpa non quia.


### Pipes and Connecting Commands

* Sometimes it's useful to output the results of a command to a text file for further analysis, reference, or processing. Try running `ls > files.txt`. Notice that the file `files.txt` was created. View that file using `more`. *What do you see in the `files.txt` file?*  
LICENSE
README.md
challenge_files
files.txt
nix_scavenger_hunt.md
nix_scavenger_hunt_stretch.md
super_scavengers.md

* Notice that if you run `ls -alh` in the `challenge_files` directory, the files scroll by very quickly. Sometimes it would be better to get the results in a paginated format. Try running `ls -alh | more`. *Describe what you see when you run `ls -alh | more`.*
total 48K
drwxrwxr-x  4 cabox cabox 4.0K Apr 14 19:13 .
drwxr-xr-x 11 cabox cabox 4.0K Apr 14 18:55 ..
drwxrwxr-x  8 cabox cabox 4.0K Apr 14 18:23 .git
-rw-rw-r--  1 cabox cabox 1.1K Apr 14 18:23 LICENSE
-rw-rw-r--  1 cabox cabox 2.7K Apr 14 18:23 README.md
drwxrwxr-x  7 cabox cabox 4.0K Apr 14 18:23 challenge_files
-rw-r--r--  1 cabox cabox  116 Apr 14 19:13 files.txt
-rw-rw-r--  1 cabox cabox 8.5K Apr 14 18:55 nix_scavenger_hunt.md
-rw-rw-r--  1 cabox cabox  317 Apr 14 18:23 nix_scavenger_hunt_stretch.md
-rw-rw-r--  1 cabox cabox  191 Apr 14 18:23 super_scavengers.md

* Earlier, when you viewed the list of active processes on your devbox using `ps aux`, the list was probably really long. You can make this list more manageable by using the pipe (`|`) to filter the results of `ps` using `grep`. Run `ps aux | grep <your_username>` to see what processes are running for your specific user. *Paste the list of processes that reference your username here:* cabox     1889  0.0  0.1   8816   768 pts/0    S+   19:33   0:00 grep --color=auto jeffe8










