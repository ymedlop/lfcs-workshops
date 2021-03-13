# [LFCS Practice Questions](https://training.linuxfoundation.org/wp-content/uploads/2019/04/LFCS-Practice-Questions-v1.0.pdf)

## Question 1
The following tasks may be achieved using the user student’s sudo privileges:
1. Temporarily mount the filesystem available on /dev/xvdf2 under /mnt/backup/.
2. Decompress and unarchive the /mnt/backup/backup-primary.tar.bz2 archive into /opt/. This should result in a new directory (created from the archive itself) named /opt/proddata/.

### Solution
````
sudo -i
mount /dev/xvdf2 /mnt/backup`
tar clvf /mnt/backup/backup-primary.tar.bz2 /opt/proddata
````

## Question 2
Configure the swap partition /dev/xvdi1 so that it does not become attached automatically at boot time.

### Solution
````
sudo nano /etc/fstab
````

## Question 3
Configure the system so that the existing filesystem that corresponds to /staging gets persistently mounted in read-only mode.

### Solution
````
sudo nano /etc/fstab
````
