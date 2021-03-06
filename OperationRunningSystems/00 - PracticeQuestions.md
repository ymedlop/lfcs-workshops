# [LFCS Practice Questions](https://training.linuxfoundation.org/wp-content/uploads/2019/04/LFCS-Practice-Questions-v1.0.pdf)

## Question 1
Create a bash shell script named certscript.sh under /home/student/apps/.
* Make sure the script can be invoked as ./certscript.sh.
* The first line of output from the script should consist of the name of the user who invoked it.
* The second line of output should contain the IP address of the default gateway.

### Solution
1. touch /home/student/apps/certscript.sh
2. chmod +x /home/student/apps/certscript.sh
3. whoami > /home/student/apps/certscript.sh
4. ip route | grep default | cut -d ' ' -f 3 >> /home/student/apps/certscript.sh

## Question 2
Install the tmux package on your system.

### Solution
1. sudo apt install tmux

## Question 3
Alter the init boot sequence so that the rc.local or boot.local script (depending on the distribution that you have selected) is executed at boot time.

### Solution
TODO:

## Question 4
Create a cron job that kills all processes named scan_filesystem which is owned by root, every minute.

### Solution
TODO: