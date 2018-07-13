---
date: 2012-08-31T09:00:13Z
tags:
- Powershell
title: Sublime Text 2 with Powershell
slug: SublimeText-With-Powershell
disqus_url: https://www.tiernanotoole.ie/2012/08/31/SublimeText-With-Powershell.html
disqus_identifier: https://www.tiernanotoole.ie/2012/08/31/SublimeText-With-Powershell.html
aliases:
- /2012/08/30/SublimeText-With-Powershell.html
---
 My new Favorite cross platform text editor is [Sublime Text 2][1]. It works on Windows, Mac OS and Linux, and i am very happy with it. My only problem is the path to start it is not exactly easy to type... So, with the help of PowerShell, my new favorite command line tool on Windows, i added an alias:

`Set-Alias subl 'c:\program files\sublime text 2\sublime_text.exe'`

I added this to my Microsoft.PowerShell_profile.ps1 file in Documents\WindowsPowerShell folder. If you don't have one of these files, check out this [Computer Performance.Co.UK post on Creating PowerShell profile files][2] and then edit the file and add the line above... Now, I can edit files in PowerShell with Sublime Text 2 by typing:

`subl filename`

Happy days!

[1]:http://www.sublimetext.com/2
[2]:http://www.computerperformance.co.uk/powershell/powershell_profile_ps1.htm