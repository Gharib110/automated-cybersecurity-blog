---
title: Stealth Alternate Data Streams and Other ADS Weirdness
date: 2011-09-20T09:25:00.000-04:00
draft: false
type: posts
summary: I was reading an article on MSDN regarding the naming of files, paths, and namespaces[1] and I discovered some interesting peculiarities regarding the naming and creation of certain files containing alternate data streams.I started by playing around with naming files based upon reserved device names "CON, PRN, AUX, NUL, COM1,
categories: Alternate Data Streams
---
# Stealth Alternate Data Streams and Other ADS Weirdness
 <br/>
 <br/>

I was reading an article on MSDN regarding the naming of files, paths, and namespaces\[[1](#8_1)\] and I discovered some interesting peculiarities regarding the naming and creation of certain files containing alternate data streams.  
  
I started by playing around with naming files based upon reserved device names "CON, PRN, AUX, NUL, COM1, LPT1, etc." As an example:

  
C:\\temp>echo hi > \\\\?\\C:\\temp\\NUL  
  

Note that this file can only be created when the prefix "\\\\?\\" or "\\\\.\\GLOBALROOT\\Device\\HarddiskVolume\[n\]\\" is appended. Subsequently, this is also the only way to delete the file.  
  
This technique has been known about for over a year now and is well documented\[[2](#8_2)\]\[[3](#8_3)\].  
  
What I found to be interesting is that when you create an alternate data stream that is attached to a file named after any reserved device name, the alternate data stream is invisible to both 'dir /R' and streams.exe unless you append the "\\\\?\\" prefix to the path. Also, if the ADS happens to be an executable, it can be executed using WMIC. As an example:

  
C:\\temp>type C:\\Windows\\System32\\cmd.exe > \\\\?\\C:\\temp\\NUL:hidden\_ADS.exe  
  
C:\\temp>dir /r C:\\temp  
  
 Directory of C:\\temp  
  
09/17/2011  06:35 AM    <DIR>          .  
09/17/2011  06:35 AM    <DIR>          ..  
09/17/2011  06:37 AM                 5 NUL  
               1 File(s)              5 bytes  
  
C:\\temp>streams C:\\temp  
  
Streams v1.56 - Enumerate alternate NTFS data streams  
Copyright (C) 1999-2007 Mark Russinovich  
Sysinternals - www.sysinternals.com  
  
No files with streams found.  
  
C:\\temp>wmic process call create \\\\?\\C:\\temp\\NUL:hidden\_ADS.exe  
Executing (Win32\_Process)->Create()  
Method execution successful.  
Out Parameters:  
instance of \_\_PARAMETERS  
{  
        ProcessId = 1620;  
        ReturnValue = 0;  
};  
  

[![](http://4.bp.blogspot.com/-kUsjHsswmv8/TniRGrpItcI/AAAAAAAAACE/cAI5JY7nh04/s400/hiddenADS.png)](http://4.bp.blogspot.com/-kUsjHsswmv8/TniRGrpItcI/AAAAAAAAACE/cAI5JY7nh04/s1600/hiddenADS.png)

  
So what are the implications of this?  
  

1) You have a file that's nearly impossible to delete unless you know to append '\\\\?\\'  
2) You can hide malicious files/executables within the device name file in an ADS that is undetectable using traditional tools.  
3) If an executable is hidden in the invisible ADS, it can be executed via WMIC.  
  
As an added comment, according to the same MSDN article: "characters whose integer representations are in the range from 1 through 31, except for alternate data streams where these characters are allowed." This would allow someone to create an ADS using alt-characters. As an example:

  
C:\\temp>echo hi > C:\\temp\\test.txt  
  
C:\\temp>echo secret text > C:\\temp\\test.txt:^G^G^G  
  
C:\\temp>dir /R C:\\temp  
  
 Directory of C:\\temp  
  
09/17/2011  07:09 AM    <DIR>          .  
09/17/2011  07:09 AM    <DIR>          ..  
09/17/2011  07:08 AM                 5 test.txt  
                                    14 test.txt::$DATA  
               1 File(s)              5 bytes  
  
C:\\temp>more < C:\\temp\\test.txt:^G^G^G  
secret text  
  
The ADS is named after three system bell characters <ALT+007>. Therefore, nothing is printed but a directory listing would yield three audible beeps. Hehe. Nothing mind-blowing but just another way to mess with admins or incident handlers.  
  
  

[![](http://2.bp.blogspot.com/-LaMChda7vBY/TniQY4VVpDI/AAAAAAAAACA/wk5at9vKSd4/s1600/smiley.png)](http://2.bp.blogspot.com/-LaMChda7vBY/TniQY4VVpDI/AAAAAAAAACA/wk5at9vKSd4/s1600/smiley.png)

Happy ADS created using <ALT-002>

  
The bottom line: these techniques would serve as both a good malware persistence mechanism and serve to frustrate any incident handler.  
  
1\. Microsoft, "Naming Files, Paths, and Namespaces", [http://msdn.microsoft.com/en-us/library/aa365247(VS.85).aspx](http://msdn.microsoft.com/en-us/library/aa365247\(VS.85\).aspx)  
  
2\. Dan Crowley, "Windows File Pseudonyms," April 2010, [http://www.sourceconference.com/publications/bos10pubs/Windows%20File%20Pseudonyms.pptx](http://www.sourceconference.com/publications/bos10pubs/Windows%20File%20Pseudonyms.pptx)  
  
3\. Mark Baggett, "NOT A CON!!!! (it's a backdoor)," February, 15 2010, [http://pauldotcom.com/2010/02/deleting-the-undeleteable.html](http://pauldotcom.com/2010/02/deleting-the-undeleteable.html)

![](https://blogger.googleusercontent.com/tracker/6052198192158185644-3478590721505682921?l=exploit-monday.com)

<br/>
Source: /feeds/3478590721505682921/comments/default
---
