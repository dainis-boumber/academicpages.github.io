---
title: "Preventing DDoS Attacks on Call Centers"
excerpt: "Product that uses deep packet inspections of IP-based phone calls and applies machine learning to analyze metadata from calls"
collection: portfolio
---

Challenge
----
It has become a regular occurrence to hear of breaches hitting private companies, the government, retailers, airlines, banks, law firms and, now, even 911 dispatch centers. Hackers engage in blackmail, trying to extort payment in return for not launching an attack that would make access to emergency services unavailable. After an attack in New York caused an outage that lasted several hours, the FBI and DHS issued security alert warnings to call centers of the danger of such attacks. Another scenario played out in California which involved tens of thousands of prank calls. Many call centers are traditionally understaffed. In IoT world, even dead cell phones not connected to a service can be hacked to make 70 calls per minute - and newer centers allow for VoiP calling, meaning any gadget can be used for the task. 
Any organization that relies on network resources, even an emergency management system, is considered a potential target, and the current environment offers many advantages to the attacker. As 911 emergency services consolidate to share infrastructure and resources and as more systems become connected to and reliant upon the Internet, these systems become vulnerable to DDoS attacks. 
Security solutions designed for enterprise customers and governments are not very helpful in such cases. One example of this was in Kansas with it’s statewide cloud-based NG911 solution hosted, secured and managed by AT&T, who built the private cloud in 2015 by utilizing data centers in Wichita and Topeka. It offers better network security and protection from other networks than other centers; Individual 911 call centers log in to NG911 through a high-speed VPN. To ensure secure 911 communications, each dispatch center uses a dedicated router to connect to the service provider, and a dedicated switch for dispatchers’ computers. Other networks can’t touch it, and it can’t­connect to the web. But that will soon change: Kansas has added text message capabilities, and will soon allow the public to send photos and video to provide dispatchers and first responders with more detail during an emergency. The existing solution will need to be updated or replaced.
 
To address the issue, the Department of Homeland Security has issued a number of large grants to various universities and companies. We worked with the University of Houston as well as a number of other enterprises that the university team chose to contract to develop a solution. The goal was to develop low-cost mitigation strategies to significantly strengthen the resilience of emergency response systems against DDoS attacks. 

My Role
----
Over the span of the project, my role shifted from research scientist to developer and finally to a CTO. Throughout the project I had interacted in various ways with university faculty, private sector contractors and senior government officials such as director of HSARPA.

Solution
----
First a vulnerability analysis was performed in order to proactively identify potential weaknesses that need to be fortified to prevent an attack. This analysis used our experts’ knowledge of security, networking, and pattern analysis.
Second, we developed mitigation strategies, solutions and best practices for how to respond if a security breach does occur
The third task is to make the results readily accessible and adaptable by emergency service providers, providing a layman-friendly plan with liaisons to help emergency call centers adopt and implement the recommendations developed by the researchers. 
This use case is an example of a project currently being tested - it is in the last year of what has been a 4 year long contract Current solution uses deep packet inspections of IP-based phone calls and applies machine learning to analyze metadata from calls — including phone numbers, call origination and service providers — to determine whether calls represent true emergencies During a DDoS attack, our algorithm can home in on what is more likely to be a real emergency. It can categorize calls and rank them based on the likelihood that they are real.
The challenge is of course that we cannot really afford to make a mistake and deny a genuine call. 
The system is currently being tuned using real life situations to find the threshold we must set in order to maximize that benefits while not increasing risks in any way.

Results
----
Based on preliminary testing, the project has been successful. It is on track for completion in 2018
The solution will be adopted by 911 call centers in 2019

Conclusions and Future Work
----
In this undertaking we were a part of a big project involving multiple teams. The project span several years, and we found new and interesting challenges in adapting to the constantly changing environment and requirements as well as frequent changes in personnel involved. In the end, the project is heading for a successful finish. In the future, we may apply the knowledge gained from working on this problem to tasks involving machine learning, security, cloud, IoT and telecommunications.

