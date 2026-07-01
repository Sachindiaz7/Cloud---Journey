#Day 6 – Users & Groups (Linux Administration)

#What is a User?

A user is an account that can log in and use the Linux system.

There are two main types of users:

- Normal User
- Root User

#Normal User

A normal user is used for everyday work.

Examples:
- Creating files
- Editing files
- Running programs

A normal user has limited permissions.

Example:
```bash
whoami
```

Output:

```text
sachi

#Root User

The root user is the administrator of Linux.

#The root user can:
- Install software
- Remove software
- Create users
- Delete users
- Change file permissions
- Modify system files

Root has almost complete control over the operating system.

#sudo (SuperUser DO)

`sudo` allows a normal user to execute **one command** with root privileges.

Example:

```bash
sudo apt update
```

Important:

- I am logged in as **sachi**.
- `sudo` temporarily uses **root privileges**.
- After the command finishes, I am still **sachi**.

#whoami

Displays the username of the currently logged-in user.

Example:

```bash
whoami
```

Output:

```text
sachi
```

#id

Displays detailed information about the current user.

Example:

```bash
id
```

Shows:

- UID (User ID)
- GID (Group ID)
- Groups

#su (Switch User)

`su` means **Switch User**.

It switches from one user account to another.

Example:

```bash
su -
```

Unlike `sudo`, `su` changes the current user until you exit.

#Home Directory

Every user has a personal home directory.

Example:

```text
/home/sachi
```

Root user's home directory:

```text
/root
```

Shortcut:

```bash
cd ~
```

For me:

```text
~
=
/home/sachi
```

#Groups

A group is a collection of users.

Groups make permission management easier.

Example:

Python Developers
- Alice
- Sachin
- Rahul

Instead of giving permissions to each user separately, Linux gives permissions to the group.

# Important Commands

```bash
whoami
id
sudo
su
cd ~
```

#Real World Example

A software company has different teams:

- Python Developers
- Java Developers
- Flutter Developers
- DevOps Engineers

Each team can have its own Linux group.

Permissions are assigned to the group instead of individual users.

This makes administration easier.

#Day 6 Summary

* Users

* Normal User

* Root User

* sudo

* whoami

* id

* su

* Home Directory

* Groups

#What I Learned Today

- Linux uses users and groups for security.
- The root user has administrator privileges.
- `sudo` temporarily runs one command with root privileges.
- Every user has a separate home directory.
- Groups make permission management easier.
