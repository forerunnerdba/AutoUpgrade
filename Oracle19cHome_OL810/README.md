Oracle Database 19c Home Installation Using AutoUpgrade on Oracle Linux 8.10

This repository contains the tested commands and execution output used to install a fresh Oracle Database 19c Home on Oracle Linux 8.10 using AutoUpgrade Patching.

Environment

Oracle Linux 8.10

Oracle Database 19c

Target RU: 19.32

AutoUpgrade Patching: 26.5.260807

Oracle Home: /u01/app/19.32.0/db

What This Log Covers

OS prerequisites and Java installation

Storage and swap preparation

AutoUpgrade download and configuration

AutoUpgrade keystore setup for MOS access

Download of Oracle 19.32 Gold Image, OPatch, and OJVM

Oracle Home creation using -mode create_home

Monitoring AutoUpgrade stages with status, lsj, tasks, and logs

Execution of root.sh and orainstRoot.sh

Successful completion of the Oracle Home installation

The AutoUpgrade job completed successfully with:

Jobs finished : 1
Jobs failed   : 0

Execution Log

Refer to the uploaded execution log for the complete commands and outputs.

Note

This exercise installs and patches the Oracle Database software home only. Database creation using DBCA or migration/upgrading of an existing database is a separate activity.

Reference

Special thanks to Daniel Overby Hansen for his article:

AutoUpgrade New Features: Install Oracle Home on Brand-New, Empty Server

https://dohdatabase.com/2025/06/17/autoupgrade-new-features-install-oracle-home-on-brand-new-empty-server/

If you find this useful, feel free to ⭐ the repository.
