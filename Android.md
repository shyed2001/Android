# Android
 ## Android Workflow
 
* 
 
 
 
 
 
# Problems and Issues with Android developmen and Fixes:

## Intel HAXM Installation /  Uninstallation failed in Android studio SDK manager

```shell
>PowerShell 7.1.3
Copyright (c) Microsoft Corporation.

https://aka.ms/powershell
Type 'help' to get help.

PS C:\Users\shyed> C:"Program Files"\Intel\HAXM\checktool.exe --verbose
CPU vendor * GenuineIntel
Intel64 supported * Yes
VMX supported * Yes
VMX enabled * Yes
EPT supported * Yes
NX supported * Yes
NX enabled * Yes
Hyper-V disabled * Yes
OS version * Windows 10.0.19043
OS architecture * x86_64
Guest unoccupied * Yes. 0 guest(s)
PS C:\Users\shyed> echo %ERRORLEVEL%
%ERRORLEVEL%
PS C:\Users\shyed> bcdedit /set hypervisorlaunchtype off
The operation completed successfully.
PS C:\Users\shyed> echo %ERRORLEVEL%
%ERRORLEVEL%
PS C:\Users\shyed> C:"Program Files"\Intel\HAXM\checktool.exe --verbose
CPU vendor * GenuineIntel
Intel64 supported * Yes
VMX supported * Yes
VMX enabled * Yes
EPT supported * Yes
NX supported * Yes
NX enabled * Yes
Hyper-V disabled * Yes
OS version * Windows 10.0.19043
OS architecture * x86_64
Guest unoccupied * Yes. 0 guest(s)
PS C:\Users\shyed> echo %ERRORLEVEL%
%ERRORLEVEL%
PS C:\Users\shyed>

```

### run below command to see whether the output is 0 after running checktool.exe?

```shell
>echo %ERRORLEVEL%
```

If the output is not 0, try to run below command to disable Hyper-V and reboot your Windows.

```shell
>bcdedit /set hypervisorlaunchtype off
```

This was helpful.
-----

But could not run emulator on android studio.
--------
> ### If having problem running Android Emulator with API level 30 , Move down and install Lower level API and Android versions.

> ### Or Can Use Online Emulator to upload and test / run apk.

> ### Or can use an actual android device

 
- solution-: Restart Your PC, it works in many cases.

- solution-: AVD Manager - Edit - Graphics : From Automatic(by default) change to Software.




