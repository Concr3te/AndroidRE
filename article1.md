
AndroidRE
-----------
This is my second attempt at reverse engineering. My first attempt at Reverse Engineering was probably done around 3 years ago, just around the same time of the year and around very late in the previous year. The attempt was at reverse engineering a Windows application, to be more specific, Metatrader, an application that is used for trading currencies, shares etc etc. It has an online store which has a lot of automated traders but which go for a price. 

My attempt, then, had mostly to do with checking for the possibility of using the automated traders without having to pay for them. It turned out that these folks were more than prepared for this, though and the application contained all sorts of mechanisms to hinder reverse engineering, including but not limited to obfuscation, which turned out to be the hardest to get around.

This time around, Reverse Engineering is against an Android Application which hopefully does not have anti-reverse engineering mechanisms built around it. First would probably be to ascertain the file format, target architecture, virtual addressing and a lot of other imformation that could prove value-able for the dissassembly/analysis/Reverse Engineering that is presumably missing as can be seen from radare2

[(image)]

The binary does load, nonetheless and seems to target x86 architecture as can be seen from the x86 specific instructions from the dissasembly.

[(image)]

APK file format seems to be mostly a ZIP file which can actually even be extracted even though the signature seems to be reversed, as per the specification which is not exactly official.


It was possible to unzip this file just normally 



First Attempt
--------------
