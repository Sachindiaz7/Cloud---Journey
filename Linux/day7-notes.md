#Day 7 - Linux Users & Groups (Part 1)

#What is a User?

A user is an identity in Linux.

Every person who uses a Linux system gets their own account.

Each user has:

- Username
- Password
- User ID (UID)
- Home Directory
- Groups

#Why Does Linux Have Users?

Linux creates users to:

- Keep the system secure
- Separate each user's files
- Avoid accidental changes
- Identify who performed an action
- Organize the operating system

Every person should have their own account.

#whoami

Purpose:

Shows the current logged-in username.

Example:

```bash
whoami
```

Output:

```text
sachi
```

Linux tells me who is currently using the terminal.

#id

Purpose:

Shows detailed information about a user.

Example:

```bash
id
```

Output:

```text
uid=1000(sachi)
gid=1000(sachi)
groups=1000(sachi),27(sudo)

It displays:

- User ID (UID)
- Group ID (GID)
- Group Memberships.

#groups

Purpose:

Shows the groups that the current user belongs to.

Example:

```bash
groups
```

Output:

```text
sachi sudo
```

It does NOT show all members of a group.

It only shows the current user's groups.

#sudo

Purpose:

Allows a normal user to execute one command with administrator (root) privileges.

Example:

```bash
sudo adduser arun
```

After the command finishes, I automatically return to being a normal user.

Identity does not change.

Only permission changes temporarily.

#adduser

Purpose:

Creates a new Linux user.

Example:

```bash
sudo adduser lucho
```

Linux automatically:

- Creates the user
- Creates a Home Directory
- Creates a Primary Group
- Assigns UID
- Assigns GID
- Sets a password

#Home Directory

When Linux creates a new user, it automatically creates:

```text
/home/lucho
```

Every user gets a separate workspace.

This keeps files:

- Secure
- Organized
- Independent

#ls vs ls /home

```bash
ls
```

Lists the contents of the current working directory.

Example:

```text
Cloud---Journey
practice

Lists the contents of the `/home` directory.

Example:

```text
sachi
lucho
```

#DevOps Scenario

A new developer joins the company.

Instead of sharing another user's account, the administrator creates a new Linux account.

Example:

```bash
sudo adduser developer1
```

Linux automatically prepares:

- User
- Password
- Home Directory
- Group

Now the developer has a secure personal workspace.

#My Understanding

Today I understood that creating a user is much more than creating a username.

Linux also creates:

- Identity
- Home Directory
- Primary Group
- UID
- GID

Everything in Linux starts with a user's identity.

A user is like the entrance (door) to everything Linux manages for that person.

Without the user, Linux doesn't know:

- Which files belong to whom
- Which home directory to open
- Which permissions to apply

My biggest realization today:

"If the door didn't open, how do we get there?"

That idea helped me understand why Linux starts with users before files and permissions.
