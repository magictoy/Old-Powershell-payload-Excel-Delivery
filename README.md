Powershell-payload-Excel-Delivery
=================================

Follow me on Twitter: @enigma0x3

Contains automatic persistence.


Persist.vbs, a 32 bit payload and the bat file need to be accessible to the target (such as a webserver). 

This attack uses an excel document to get into the organization (bypassing filters and scans), determines the system's architecture, pulls down the payload and executes it. It then pulls down a persistence script, drops it, creates a registry key for autorun for the persistence script. Once done, it also drops a self-deleting bat file that removes the initial payload from the system.

Once the payload is ran, it runs in the powershell process, so if the user closes excel, you keep your shell. You also remain in a stable process until reboot, so migration is not needed. AV also does not pick this up.

Shoutout to @TheColonial for helping me with the code for hiding the window upon payload execution and testing the code as it was developed. Big thanks mate :)

PowerSploit Function: Invoke-Shellcode
Author: Matthew Graeber (@mattifestation)
License: BSD 3-Clause
Required Dependencies: None
Optional Dependencies: None
