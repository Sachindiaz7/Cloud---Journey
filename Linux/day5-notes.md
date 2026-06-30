#️⃣#Day 5 – Package Management (APT)

#What?

APT (Advanced Package Tool) is Ubuntu's package manager.

It is responsible for:

#Installing software
* Updating package information
* Upgrading installed software
* Searching packages
* Displaying package details
* Removing software
* Cleaning unused packages

#Why?

Without APT:

* Software installation would be manual.
* Dependencies would be difficult to manage.
* Updates would be time-consuming.
* System maintenance would become harder.

#How?
You
 │
 ▼
APT
 │
 ▼
Ubuntu Repository (Internet)
 │
 ▼
Downloads Package Information
 │
 ▼
Installs / Updates / Removes Packages

#Where?

APT is used on:

Ubuntu Desktop
Ubuntu Server
AWS EC2 (Ubuntu)
Azure Ubuntu VM
Google Cloud Ubuntu VM
Any Debian-based Linux distribution

#What if I don't use it?
* Software must be installed manually.
* Dependency management becomes difficult.
* Missing security updates.
* Increased chance of installation errors.

#Real DevOps Example

A DevOps engineer launches a new Ubuntu server and needs Git.

Instead of downloading Git manually:

sudo apt install git

Ubuntu downloads, installs, and configures Git automatically.

#️#Commands
 
1. Check APT Version
apt --version
#What?

Displays the installed version of APT.

#Why?

To verify that APT is available and check its version.

#What changed?

Nothing.

It only displays information.

2. Install Package
sudo apt install git

#What?

Installs Git.

#Why?

To install software from Ubuntu repositories.

What changed?

Git becomes available on your Ubuntu system.

3. Update Package List
sudo apt update

#What?

Downloads the latest package information.

#Why?

Ubuntu needs the latest package list before installing or upgrading software.

Important

❌ Does NOT upgrade software.

✅ Only updates the package list.

4. Upgrade Installed Packages

sudo apt upgrade

#What?

Upgrades installed software.

#Why?

To receive:

* Security patches
* Bug fixes
* Performance improvements
* New features

#Real-life Example

Updating Chrome from Version 135 to Version 136.

What changed?

Installed packages move to newer versions.

Example:

Git 2.52
      ↓
Git 2.53

5. Search Packages
apt search docker

Searches every package related to the keyword.

For a more precise search:

apt search ^docker.io

#Why?

To find the correct package before installing it.

What changed?

Nothing.

Ubuntu only displays matching packages.

6.Show Package Details
apt show git

Displays:

Package Name
* Version
* Maintainer
* Dependencies
* Installed Size
* Description

7. Remove Package
sudo apt remove git

#What?

Removes the package.

#Why?

When software is no longer required.

What changed?
* Package removed.
* Configuration files remain.

8. Purge Package
sudo apt purge git

#What?

Completely removes the package.

#Why?

To perform a clean removal.

What changed?
Package removed.
Configuration files removed.

9. Remove Unused Dependencies
sudo apt autoremove

#What?

Removes dependency packages that are no longer required.

#Why?

Keeps the system clean and frees storage.

What changed?

Unused dependency packages are removed.

#Hands-on Practice

apt --version

sudo apt install git

sudo apt update

sudo apt upgrade

apt search docker

apt search ^docker.io

apt show git

Note: Do not run sudo apt remove git or sudo apt purge git right now because Git is required for our DevOps journey.

#Mini Challenge

1. Explain the difference between apt update and apt upgrade.
2. Explain the difference between apt remove and apt purge.
3. Why is apt search useful?
4. What details does apt show display?
5. Which command removes unused dependency packages?

#Key Learnings

* APT is Ubuntu's package manager.
* apt update refreshes the package list.
* apt upgrade upgrades installed software.
* apt search finds packages.
* apt show displays package details.
* apt remove removes software while keeping configuration files.
* apt purge removes software and configuration files.
* apt autoremove cleans unused dependency packages.

#Connection

Day 5 explained how Ubuntu manages software.

➡️ Next: Day 6 – Users & Groups

We'll answer questions like:

 * Who is allowed to install software?
 * Why do we use sudo?
 * What is the root user?
 * How does Linux decide who has permission to perform administrative tasks?
