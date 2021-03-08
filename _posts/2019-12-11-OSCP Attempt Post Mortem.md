---
tag: ["Pen Testing with Kali"]
title: Journey Through PWK - 5 - Attempt 1 Post Mortem
---
# Journey through PWK - Attempt 1 Post Mortem

My first attempt to earn the OSCP was not successful in terms of earning the certification. Although, it was a great success In learning about the exam format as well as what skills I need to work on for attempt number two. I do not consider this a failure in the slightest because it was a fantastic learning opportunity. If you can take anything away from this post remember that failing doesn’t make you a failure and a true failure is not learning from the experience.

Now, I am going to take some time to discuss my methodology, how it worked out, and lessons learned. Also, links to previous posts about how I prepared can be found at the bottom of this post.  

## Attack Methodology
I have read a number of write ups and spoke to others who have taken the OSCP and I took what they had to say and used it to define how I would go about taking my exam. My plan was to kick off some automated network scans that would organize results by host (AutoRecon is a glorious tool), work on the buffer overflow challenge, and then move on to trying to root the high point value devices. I also planned to take breaks every second or third hour into the exam, stop every hour to examine if I was in a rabbit hole by asking enumeration questions, eat, and take one to two naps.

## Overflowin’
I knew it would take some time to complete the buffer overflow and it was also the thing I was most concerned about doing. Fortunately my studying and preparation of this paid off and I was able to complete this challenge. Although I think it took me much longer than it should have due to not identifying all the bad characters which was a mix of my poor eye sight and inputting all the characters at once. After completing the overflow challenge, about two or three hours in I broke for lunch.

## Shoot for Shells
I moved to reviewing my enumeration results and searching online for potential vulnerabilities associated with the services that were running on devices. I was able to obtain a local shell on a high point value box in about two or three hours of moving between devices trying different things. After gaining a shell as a low privilege user on a Unix system I enumerated the device looking for what was installed, what was running, schedule tasks, file permissions, etc. I spent a very long time trying to escalate my permissions with no success.

It was starting to get late, I was getting discouraged as well as tired with my lack of success getting a shell. I was back to bouncing back and fourth between hosts trying different things with no success. At midnight, about 14 hours into the exam time, I had not made any significant progress since getting the local shell on a box and decided it was time to cut my losses and sleep.

## Morning Mourning
The next morning at about 7 AM I woke up, made my coffee, and use my last two hours to try for a shell. No shells were gained.

Honestly, I was sad that I didn’t end up getting more shells but I didn’t dwell on that too long because I knew it would not be helpful in the long run. I changed my outlook to see this an opportunity to see where I need to improve and as an experience to share with the community to help others.

## Lessons Learned

In general, look for bad characters in smaller chunks to avoid mistakes. If you are like me and have poor eye sight this is really important.
Build a better profile of each device and research exploits as to not waste time trying an exploit that is not relevant.

I attempted to exploit a host using an exploit that would work successfully but the payload would not execute because the host was on a version that did not have technology to execute the payload. I would have found that had I done a better job researching the exploit and host.

## What next?
My plan now is to spend time on Hack the Box rooting OSCP like boxes (https://docs.google.com/spreadsheets/d/1dwSMIAPIam0PuRBkCiDI88pU3yzrqqHkDtBngUHNCw8/edit#gid=1839402159) and when I am stuck follow along with these walkthrough’s (https://www.youtube.com/playlist?list=PLidcsTyj9JXK-fnabFLVEvHinQ14Jy5tf).
Also, I plan on reviewing the information in one of the best compilation of resources around:
https://www.netsecfocus.com/oscp/2019/03/29/The_Journey_to_Try_Harder-_TJNulls_Preparation_Guide_for_PWK_OSCP.html  
