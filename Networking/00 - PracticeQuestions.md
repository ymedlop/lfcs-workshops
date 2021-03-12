# [LFCS Practice Questions](https://training.linuxfoundation.org/wp-content/uploads/2019/04/LFCS-Practice-Questions-v1.0.pdf)

## Question 1
1. Find the name of the service which uses TCP port 2605, as documented in /etc/services, and write the service name to the file /home/student/port-2605.txt.
2. Find all of the ports used for TCP services IMAP3 and IMAPS, again as documented in /etc/services, and write those port numbers to the file /home/student/imap-ports.txt.

### Solution
1. `cat /etc/services | grep -i 2605 | cut -f1 > /home/student/port-2605.txt`
2. `cat /etc/services | grep -iE 'IMAP3|IMAPS' | cut -f3 > /home/student/imap-ports.txt`