# HiveJack
This tool can be used during internal penetration testing to dump Windows credentials from an already-compromised host. It allows one to dump SYSTEM, SECURITY and SAM registry hives and once copied to the attacker machines provides an option to delete these files to clear the trace.

Often, this is a repetitive process, once an attacker gets system-level access on the compromised host dumping hives values is the next step. Time is very valuable when it comes to internal penetration testing. **HiveJack** will save you plenty of time when it comes to dumping and deleting the files. You'll never have to remember the command to perform the actions. ;)

![image](https://user-images.githubusercontent.com/3501170/79689138-2d9a1780-8296-11ea-9d7f-35a02ad7e41d.png)

Files dumped in the *c:\\temp\\* folder of the compromised host:

![image](https://user-images.githubusercontent.com/3501170/80096475-f769da00-85ac-11ea-99e1-e47dff224b4a.png)

Files are successfully deleted from the compromised host upon clicking on the **Delete Hives** button:

![image](https://user-images.githubusercontent.com/3501170/80096814-8aa30f80-85ad-11ea-9c1a-1559348c9f69.png)

Any suggestions or ideas for this tool are welcome - just tweet me on [@ManiarViral](https://twitter.com/maniarviral)

A hive is a logical group of keys, subkeys, and values in the registry that has a set of supporting files loaded into memory when the operating system is started or a user logs in.

Registry files have the following two formats:
  - Standard format: Supported from Windows 2000, also supported in the later versions of the Windows for backward compatibility
  - Latest format: Supported starting with Windows XP
  
**HKEY_CURRENT_USER, HKEY_LOCAL_MACHINE\SAM, HKEY_LOCAL_MACHINE\Security, and HKEY_USERS\.DEFAULT;** all other hives use the latest format.

During an internal penetration test, the attacker often wants to perform a lateral movement from one host to the other. To move from one host to the other attacker often requires account credentials. Using **HiveJack** attacker would be able to gather credentials via system hives.

**HiveJack** is useful once the attacker has successfully gained local admin or system privileges on one of the compromised hosts. To further gain access within the network attacker can use registry hives. Dumping these hives would allow an attacker to capture system users' password hashes. 

# How do I use this?

Use a HiveJack.exe file from the release section and run it on the compromised host. The hives will get stored at the *c:\\temp\\* folder.

**Note:** Please make sure you have temp folder in the 'C:' Drive of the system before dumping the registry hives.

# Questions?

Twitter: https://twitter.com/maniarviral <br>
LinkedIn: https://au.linkedin.com/in/viralmaniar

# Contribution & License

MIT License

Copyright (c) 2020 Viral Maniar

Permission is hereby granted, free of charge, to any person obtaining a copy
of this software and associated documentation files (the "Software"), to deal
in the Software without restriction, including without limitation the rights
to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
copies of the Software, and to permit persons to whom the Software is
furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all
copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR
IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY,
FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE
AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER
LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM,
OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE
SOFTWARE.

Any suggestions or ideas for this tool are welcome - just tweet me on [@ManiarViral](https://twitter.com/maniarviral) [@PreemptiveCyber](https://twitter.com/PreemptiveCyber)
