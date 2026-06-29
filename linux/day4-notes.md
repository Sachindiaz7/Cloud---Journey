#Day 4 - Linux File Permissions

#what?

Linux file permissions determine who can read,write or execute a file or directory

There are three permission types :
* Read    (r)
* write   (w)
* Execute (x)

Permission are assigned to :
* Owner
* Group
* Others

#why?

Linux is a multi-user operating system
without file permissions,every user could modify,delete or execute every file.
Permission protect files,improve security and prevent unauthorized access.

#how?

Permission Values
permission                       value
read    (r)                        4
write   (w)                        2
execute (x)                        1

#Numeric Permissions

Number                         meaning
 7                                rwx
 6                                rw-
 5                                r-x
 4                                r--
 0                                ---
Example : 755
Owner  : rwx
Group  : r-x
Others : r-x

#where?
Linux permissions are used in :
* Linux Servers
* AWS EC2
* Docker Containers
* Kubernetes
* Jenkins
* Shell Scripts

#What if i dont use it ?

Incorrect permission can cause :
* Permission denied errors
* Script failing to execute
* Applications failing to start
* Security vulnerabilities

#Real DevOps Example

A deployment script:

deploy.sh

Without execute permission:

./deploy.sh

Output:

Permission denied

Fix:

chmod 755 deploy.sh

#Commands

Check permissions
ls -l
Change permissions
chmod 755 demo.txt
Run command as administrator
sudo apt update
Change owner
sudo chown user:user demo.txt

#Interview Questions
* What are Linux file permissions?
* What do r, w, and x mean?
* What are the values of r, w, and x?
* Explain 755.
* Explain 644.
* What does chmod do?
* What does sudo do?
* What does chown do?

#Hands-on Practice

touch demo.txt

ls -l

chmod 755 demo.txt

ls -l demo.txt

Observe the permission change.

#Mini Challenge

* Create a file named practice.txt.
* Check its permissions.
* Change the permissions to 755.
* Verify using ls -l.
* Explain what 755 means.

#Key Learnings

* Linux uses Owner, Group, and Others.
* r = 4, w = 2, x = 1.
* 644 = rw-r--r--.
* 755 = rwxr-xr-x.
* chmod changes permissions.
* sudo runs commands as an administrator.
* chown changes file ownership.

#Revision

Answer without looking at your notes:

* Why does Linux use file permissions?
* Why is 755 used for executable files?
* Why is 644 used for normal files?
* What happens if a script doesn't have execute permission?
* What is the difference between chmod and chown?

#Connection

Today's Topic:

Linux File Permissions

⬇

Tomorrow's Topic:

Package Management (apt)

Connection:

Installing software requires administrator privileges.

Example:

sudo apt update
sudo apt install git
