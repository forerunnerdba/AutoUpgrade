# Oracle Database 19c RU 19.32 on Oracle Linux 10 Using AutoUpgrade

This repository contains the complete commands and execution output from my lab where I installed **Oracle Database 19c RU 19.32 on Oracle Linux 10.2 using AutoUpgrade**.

The main goal of this test was to compare the traditional software download/install/patch workflow with the newer AutoUpgrade approach.

With AutoUpgrade, I used:

```text
One configuration file
        +
One Java command
        ↓
Gold Image + Recommended Patches
```

In my lab, AutoUpgrade downloaded the **Oracle Database 19.32 Gold Image and recommended patches in less than five minutes**.

The downloaded software included:

- Oracle Database 19.32 Gold Image
- Database RU 19.32
- OPatch
- OJVM
- Data Pump Bundle Patch
- JDK Bundle Patch
- AutoUpgrade

## Execution Log

The complete command sequence and actual execution output are available here:

👉 **[Oracle 19c_Home_Database_Install_Using_AutoUpgrade_On_OL10_Command & Execution Output](OracleDatabase19c_On_OL10_Using_AutoUpgrade.log)**

It contains the detailed commands, configuration examples, and execution output from the lab.

The log also shows AutoUpgrade creating the new Oracle Home and applying the required patches automatically through:

```bash
java -jar autoupgrade.jar \
-config install-home.cfg \
-patch \
-mode create_home
```

AutoUpgrade handled the major stages in sequence:

```text
Gold Image Extraction
        ↓
Oracle Home Installation
        ↓
RU / OJVM / JDK / DPBP Patching
        ↓
Oracle Home Completion
```

The execution completed successfully with:

```text
Jobs finished : 1
Jobs failed   : 0
```

A new **CDB and PDB** were then created successfully using DBCA on Oracle Linux 10.2.

Final validation confirmed:

- Oracle Database version **19.32.0.0.0**
- PDB opened in **READ WRITE**
- Database components at **19.32**
- Database RU, OJVM, and Data Pump Bundle Patch registered successfully
- OPatch inventory validated successfully
- **No invalid database objects**

The SQL patch and inventory validations are included in the execution log.

## Important Notes

During this test, the `oracle-database-preinstall-19c` RPM was not available through the OL10 repository configuration I was using, so the operating-system prerequisites were configured manually.

AutoUpgrade also required **Java 21** in this environment, so I explicitly installed:

```bash
dnf install -y java-21-openjdk-devel
```

## Security

Do not commit real database passwords, SSH private keys, wallet files, or other credentials to GitHub.

## Acknowledgements

Thanks to **Mike Dietrich(https://mikedietrichde.com/2026/09/24/oracle-database-19c-is-supported-on-ol-rhel-10/)** for sharing the information about Oracle Database 19c support on Oracle Linux 10 / RHEL 10, which inspired me to validate this configuration in my lab.

Thanks to **Daniel Overby Hansen** for his excellent articles and examples around the newer AutoUpgrade capabilities.

Thanks to **Tim Hall** for the Oracle Linux and Oracle Database installation documentation that helped while reviewing the manual prerequisite configuration.

I also found **Marcus Vinicius' AutoUpgrade Composer** and **Kamil Stawiarski's ALIS — Automatic Linux Installation Scripts** very useful while exploring Oracle installation and AutoUpgrade automation.

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

## Disclaimer

This repository documents my personal lab testing and learning experience.

Always validate Oracle documentation, patch requirements, security settings, and prerequisites before implementing similar steps in production.

## ⭐ Feedback

If you find this documentation useful, feel free to share your feedback, suggestions or corrections. Please consider giving the repository a Star.

The objective is to continuously improve the documentation and capture practical Oracle DBA deployment experiences.
