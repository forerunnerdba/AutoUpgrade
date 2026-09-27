# Oracle Database 19c Home Installation Using AutoUpgrade on Oracle Linux 8.10

This repository contains the tested commands and execution output used to install a fresh Oracle Database 19c Home on Oracle Linux 8.10 using AutoUpgrade Patching.

## Environment

- Oracle Linux 8.10
- Oracle Database 19c
- Target RU: 19.32
- AutoUpgrade Patching: 26.5.260807
- Oracle Home: /u01/app/19.32.0/db

## What This Log Covers

- OS prerequisites and Java installation
- Storage and swap preparation
- AutoUpgrade download and configuration
- AutoUpgrade keystore setup for MOS access
- Download of Oracle 19.32 Gold Image, OPatch, and OJVM
- Oracle Home creation using -mode create_home
- Monitoring AutoUpgrade stages with status, lsj, tasks, and logs
- Execution of root.sh and orainstRoot.sh
- Successful completion of the Oracle Home installation

The AutoUpgrade job completed successfully with:

Jobs finished : 1
Jobs failed   : 0

## Execution Log

The complete command sequence and actual execution output are available here:

👉 **[Oracle 19c_Home_Insttalation_Using_AutoUpgrade_Command & Execution Output](Oracle_19c_FreshInstall_Using_AutoUpgrade.log)**

It contains the detailed commands, configuration examples, and execution output from the lab.

Note

This exercise installs and patches the Oracle Database software home only. Database creation using DBCA or migration/upgrading of an existing database is a separate activity.

### Security

Do not commit real database passwords, SSH private keys, wallet files, or other credentials to GitHub.

### Reference

Special thanks to ***Daniel Overby Hansen*** for his article: AutoUpgrade New Features: Install Oracle Home on Brand-New, Empty Server

## 👨‍💻 Author

**Chakravarthy P**

Oracle Database Administrator / SME

Areas of interest:

* Oracle Database
* Oracle RAC
* Oracle ASM
* Oracle Data Guard
* Oracle Restart
* Oracle Cloud
* Microsoft Azure
* Database Migration
* Oracle Patching
* Ansible Automation
* Linux

## ⭐ Feedback

If you find this documentation useful, feel free to share your feedback, suggestions or corrections. Please consider giving the repository a Star.

The objective is to continuously improve the documentation and capture practical Oracle DBA deployment experiences.
