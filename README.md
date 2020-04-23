# HiveJack
This tool can be used during internal penetration testing to dump Windows credentials from an already-compromised host. It allows one to dump SYSTEM, SECURITY and SAM registry hives and once copied to the attacker machines provides an option to delete these files to clear the trace.

Often, this is a repetative process, once an attacker gets a system level access on the compromised host dumping hives values is the next step. Time is very valuable when it comes to internal penetration testing. **HiveJack** will save you plenty of time when it comes to dumping and deleteing the files. You'll never have to rememember the command to perform the actions. ;)

![image](https://user-images.githubusercontent.com/3501170/79689138-2d9a1780-8296-11ea-9d7f-35a02ad7e41d.png)

A hive is a logical group of keys, subkeys, and values in the registry that has a set of supporting files loaded into memory when the operating system is started or a user logs in.

Registry files have the following two formats:
  - Standard format: Supported from Windows 2000, also supported in the later versions of the Windows for backward capatibitlity
  - Latest format: Supported starting with Windows XP
  
**HKEY_CURRENT_USER, HKEY_LOCAL_MACHINE\SAM, HKEY_LOCAL_MACHINE\Security, and HKEY_USERS\.DEFAULT;** all other hives use the latest format.

During internal penetration test, attacker often wants to perform lateral movement from one host to the other. To move from one host to the other attacker often requires account credentials. Using **HiveJack** attacker would be able to gather credentials via system hives.

**HiveJack** is useful once the attacker have successfully gained local admin or system privileges on one of the compromised host. To further gain access within the network attacker can use registry hives. Dumping these hives would allow an attacker to capture system users' password hashes.  

