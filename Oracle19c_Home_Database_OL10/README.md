# Oracle Database 19c RU 19.32 on Oracle Linux 10 Using AutoUpgrade

After reading **Mike Dietrich’s article on Oracle Database 19c support for Oracle Linux 10 / RHEL 10**, I wanted to validate the setup myself in a fresh Oracle Linux 10.2 environment.

Instead of following the traditional Oracle Database software installation and patching approach, I decided to take the test one step further and use **AutoUpgrade** to download the required software and patches, create the Oracle Home, and apply the patches automatically.

That turned out to be the most interesting part of this lab.

Using a single AutoUpgrade configuration file and one Java command, I was able to download the **Oracle Database 19.32 Gold Image together with the recommended patches**. In my lab, the complete download took **less than five minutes**.

I then used AutoUpgrade again to create the Oracle Home and apply the required patches in sequence, significantly simplifying the traditional install-and-patch workflow.
