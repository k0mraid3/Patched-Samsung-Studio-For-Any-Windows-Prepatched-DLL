# Samsung-Studio---Patched-for-any-Windows-Device
A patched version of Samsung Studio, with the IL instructions to check device type nop'ed out. Tested on Windows 11 24H2 Build 26085 Insider build.

# Instructions to obtain and patch the Samsung Studio app on (probably) any Windows system using "Winget"

-1 Install Samsung Studio via winget using the following command.
```winget.exe install --id 9P312B4TZFFH --exact --accept-source-agreements --silent --disable-interactivity --accept-package-agreements```

-2 Find and open Samsung Studio, let the "Not a Samsung device" screen come up, open Task Manager and find the running process, then open its file location by right-clicking its entry in Task Manager and selecting "Open File Location".

-3 Now, explorer will open in the location of the VideoEditor.exe, we need to navigate UP/BACK one directory, to the packages root directory. Once there, copy all the contents of the package to a new folder on C:\ drive called "SamsungStudio" without the quotes. It will look like this ``` C:\SamsungStudio ```

-4 Still in the packages root, in the new location at C:\SamsungStudio, find a file called "AppxSignature.p7x" and delete it. 

-5 Download the patched VideoEditor.DLL from this repo, and place it in ```C:\SamsungStudio\VideoEditor``` - If prompted to overwrite an existing file with same name, click yes/confirm.

-6 Uninstall the original downloaded version of Samsung Studio.

-7 Now open Powershell as administrator, and run ```cd C:\SamsungStudio``` then run ```Add-AppxPackage -Register "C:\SamsungStudio\AppxManifest.xml```

-Fin.  Done!! Open and Enjoy! 

K0mraid x Nedry --> 03-22-2024
