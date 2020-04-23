# HiveJack
This tool can be used during internal penetration testing to dump Windows credentials from an already-compromised host. It allows one to dump SYSTEM, SECURITY and SAM i.e system hives and once copied to the attacker machines provides an option to delete these files to clear the trace.

![image](https://user-images.githubusercontent.com/3501170/79689138-2d9a1780-8296-11ea-9d7f-35a02ad7e41d.png)

A hive is a logical group of keys, subkeys, and values in the registry that has a set of supporting files loaded into memory when the operating system is started or a user logs in.

Registry files have the following two formats:
  - Standard format: Supported from Windows 2000, also supported in the later versions of the Windows for backward capatibitlity
  - Latest format: Supported starting with Windows XP
  
**HKEY_CURRENT_USER, HKEY_LOCAL_MACHINE\SAM, HKEY_LOCAL_MACHINE\Security, and HKEY_USERS\.DEFAULT;** all other hives use the latest format.
