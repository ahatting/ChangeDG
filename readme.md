## ChangeDG

_The tool allows you to change the authorized senders for Distributiongroups/lists in an on-premises Active Directory when you use Office365 and no longer have an on-premises Exchange Organization. Changes will be synchronized towards Office 365 on the next Directory Synchronization._

**minimal requirements**
- Windows PowerShell version 3
- Read/Write access to the AD attributes (below)
- Active Directory Module for PowerShell

**Instructions**
Input field
Enter the samaccountname/groupname of the user/group you want to add or remove. 1 per line (use enter)
or
Use "File - Open" to open a CSV with the samaccountnames (the CSV should have 1 header -> samaccountname , 1 name per line, no commas needed)

Sample CSV:
samaccountname
john.doe
jane.doe

Use the corresponding buttons to perform the action in Active Directory. 
The following attributes can be changed:
- authOrig: List of senders (users, not groups) that are allowed to send to the DL
- unAuthOrig: List of senders (users, not groups) to BLOCK from sending to the DL
- dlMemRejectPerms: Used in place of unAuthOrig when using security groups
- dlMemSubmitPerms: Used in place of authOrig when using security groups

**If you only want the tool and don't care about what the script does, you will only need:**
- PS-ChangeDG.exe
- PS-ChangeDG.exe.config

***

![Sample](https://github.com/ahatting/ChangeDG/blob/master/Sample1.png "ChangeDG")
