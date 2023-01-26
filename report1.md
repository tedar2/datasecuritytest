# Report h01

![HH Logo](https://github.com/tedar2/datasecuritytest/blob/b06717bd3ba1f566c179f3dc5952aa4f8ee270b7/HH%20logo.png) 

### task z)

### Hutchins et al 2011: Intelligence-Driven Computer Network Defense Informed by Analysis of Adversary Campaigns and Intrusion Kill Chains (summary)

#### Introduction

The article covers the topic of the Advanced Persistent Threats (APTs) and the challenges they pose to computer networks. APTs are a new class of threats that are focused on compromising data for economic or military purposes. Apparently, most organizations have relied on technologies and processes designed to mitigate risks associated with automated viruses and worms, which do not sufficiently address APT intrusions. Conventional incident response methods fail to mitigate the risk posed by APTs because they assume that response should happen after the point of compromise and that the compromise was the result of a fixable flaw. 

One can outline the characteristics of APTs and examples of how they have been observed and characterized by industry and the U.S. government. The advances in infrastructure management tools have enabled best practices of enterprise-wide patching and hardening, but APT actors continue to demonstrate the capability to compromise systems using advanced tools and customized malware. An intelligence-driven, threat-focused approach to study intrusions from the adversaries’ perspective, called “kill chain” analysis, that can be used to develop resilient mitigations against intruders and intelligently prioritize investments in new technology or processes.

Some key bullet points: 

+ a new class of threats emerged - "Advanced Persistent Threat" or APT 
+ conventional incident response methods fail to mitigate the risk with APT intrusions
+ APT actors continually demonstrate the capability to compromise systems by using advanced tools, customized malware, and "zero-day" exploits that anti-virus and patching cannot detect or mitigate
+ responses to APT intrusions reqiure an evolutions in analysis, process and technology
+ intelligence-driven, threat focused approach to study intrusions from the adversaries' perspective
+ each discrete phase is mapped to one step - detection, mitigation and response
+ "kill chain" - describes the structure of intrusion; throuhg this model, defenders can develop resilient mitigations against intruders 
+ "kill chain" (U.S. Department of Defence, 2007) stages are fix, track, target, engage, access

#### Chapter 3.2 and 3.3 

The Intrusion Kill Chain is a systematic process used to target and engage an adversary in order to achieve a desired effect. It consists of the phases: reconnaissance, weaponization, delivery, exploitation, installation, command and control (C2), and actions on objectives. During reconnaissance, the attacker identifies and selects targets. Weaponization involves combining a remote access trojan with an exploit into a deliverable payload. Delivery refers to the transmission of the weapon to the targeted environment. Exploitation is the triggering of the attacker's code on the victim host. Installation involves installing a remote access trojan or backdoor on the victim system. Command and control refers to the process of establishing a connection between the compromised host and an internet controller server. Finally, actions on objectives refers to the attacker's ultimate goal, which could be data exfiltration, violations of data integrity or availability, or gaining access to a victim box to compromise additional systems.

The article discusses the concept of an "intrusion kill chain," which is a systematic process used by adversaries to target and engage a victim in order to achieve their objectives. A new kill chain model is presented - specifically for intrusions. The idea of how this model can be used as a framework for actionable intelligence by aligning enterprise defensive capabilities to the specific processes an adversary undertakes to target the enterprise. By aligning defensive capabilities in this way, defenders can measure the performance and effectiveness of their actions and plan investment roadmaps to rectify any capability gaps. Then a course of action matrix is also being covered that depicts various defensive actions, such as detection, denial, disruption, degradation, deception, and destruction, that can be employed in each phase of the kill chain to increase the adversary's cost of executing successful intrusions. The article includes an example of how this approach can be used to measure the resiliency of a defender's security posture over time. 

+ courses of Action Matrix: 

![](https://github.com/tedar2/datasecuritytest/blob/c44e2d4c87cb1401f2752057fbd69432d4358340/Screenshot%202023-01-22%20at%2019.47.49.png)

+ Defenders can generate metrics of the resiliency by measuring the performance and effectiveness of defensive actions against intruders

This article provides with a nice introduction to the security world, and I have had some fun time in looking up some terminology I have not read about before and getting introduced to the concepts. 

Source:  [Hutchins et al 2011: Intelligence-Driven Computer Network Defense Informed by Analysis of Adversary Campaigns and Intrusion Kill Chains](https://lockheedmartin.com/content/dam/lockheed-martin/rms/documents/cyber/LM-White-Paper-Intel-Driven-Defense.pdf)


### Command Line Basics Revisited
+ $ pwd   /home/tero
+ pwd prints the working directory
+ $ ls  - listing files in working directory
+ $ cd  - change directory under the working directory
+ $ cd .. - change directory up
+ $ less daria.txt - view file 
+ $ ls /etc |less - any command output can be read one screenfull at a time
+ $ nano F00.TXT - easiest text editors are pico & nano
+ $ mkdir NEWFOLDER / $ mv OLDNAME NEWNAME - creating and renaming
+ $ mv SOMEFILE NEWDIR/ - copy original to copy
+ $ rmdir EMPTYDIR - remove empty directory; $ rm JUNK; $ rm -r FOLDEROFJUNK


+ $ ssh daria@example - open a remote command shell in a very secure way
+ $ remotecomputer$ exit
+ $scp -r FOLDER daria@example.com:public_html
+ $ man ls
+ $ ls --help
+ $ wget -h
+ $ sudo apt-get update
+ $ sudo apt-get purge nethack

Source: [Karvinen 2020: Command Line Basics Revisited](https://terokarvinen.com/2020/command-line-basics-revisited/)

### a) Bandit oh-five exercizes. 

I was not sure if I can list the commands and&or passwords here to avoid spoilers (and I have them saved in my notepad if needed to be demonstrated), but I attach some screenshots of the levels:

+ bandit0 level 
<img width="262" alt="image" src="https://user-images.githubusercontent.com/90892301/214106287-fc8b24c4-e753-4422-b16c-180bb5960441.png">

+ bandit1 level
<img width="262" alt="image" src="https://user-images.githubusercontent.com/90892301/214105983-253848a7-30a4-44da-b9b6-19c4281fd28d.png">

+ bandit2 level
<img width="288" alt="image" src="https://user-images.githubusercontent.com/90892301/214108292-4af32698-0181-4eff-941a-b072592c3aa4.png">

+ bandit3 level

<img width="288" alt="image" src="https://user-images.githubusercontent.com/90892301/214110517-da27a4ed-8ac5-4fd7-80fd-5dc11834cbb2.png">

+ bandit4 level

<img width="288" alt="image" src="https://user-images.githubusercontent.com/90892301/214111626-9350d5fd-5a40-4674-8ae9-2558dd884e0c.png">

Source: [OverTheWire](https://overthewire.org/wargames/bandit/)

The exercises were a real fun to do and it also helped me to refresh the command and the ssh knowledge.

### b&c) Installing Debian and the WebGoat exercise:

I am working with the MacBook Pro that has the Apple M1 Pro Chip, 32gb, and macOS Ventura 13.1 The software of my choice for installing the Debian and further WebGoat task is Parallels Desktop 18 application for Mac with the Debian GNU Linux 11.3 ARM64 image.

<img width="726" alt="Screenshot 2023-01-26 at 22 43 49" src="https://user-images.githubusercontent.com/90892301/214946382-446411e5-888c-45d3-bdf4-25b044ef8bd8.png">

I have followed the instructions from https://terokarvinen.com/2020/install-webgoat-web-pentest-practice-target/ and I have done all commands from the article as it is possible to see from the screenshots:

<img width="729" alt="Screenshot 2023-01-26 at 21 53 39" src="https://user-images.githubusercontent.com/90892301/214946250-533d1e21-356c-4b3a-b572-2c4687e3f50d.png">

<img width="723" alt="Screenshot 2023-01-26 at 21 53 57" src="https://user-images.githubusercontent.com/90892301/214946699-da2d98ee-b535-4fee-9250-4974ac96cb07.png">

This is the result of the last command (java -jar webgoat-server-8.0.0.M26.jar) result: 

<img width="723" alt="Screenshot 2023-01-26 at 21 54 37" src="https://user-images.githubusercontent.com/90892301/214946742-a7a1383f-0a5e-4bec-b8c4-e7c4ff1a058f.png">

However, I faced another peculiar issue. Even though, it seems that the installation went successful, and I am able to open up the WebGoat local host (mentioned in the original Tero's article), I get an error whenever I create the user and try to log in after that: 

<img width="887" alt="Screenshot 2023-01-26 at 22 48 15" src="https://user-images.githubusercontent.com/90892301/214947331-957d854d-a16d-4d64-bb6b-e15441b5bdc2.png">

The error:

<img width="472" alt="image" src="https://user-images.githubusercontent.com/90892301/214949076-7dc1584f-3f66-4420-8bb1-416c5ea27ad3.png">


I tried to reinstall the Debian, tried to run all commands from the article, and created different users, but for now I still come back to the same error. 

***

After several attempts of reinstalling and providing the commands, I was able to create a test user in the WebGoat and finally log in, and I managed to fulfill the exercises:

### d) Hacker warmup. Solving the following tasks

+ General: HTTP Basics

<img width="730" alt="Screenshot 2023-01-26 at 23 06 30" src="https://user-images.githubusercontent.com/90892301/214957542-8d23ae2d-8ce4-4c97-8240-43d55eb8a027.png">

<img width="1011" alt="Screenshot 2023-01-26 at 23 20 14" src="https://user-images.githubusercontent.com/90892301/214957644-156cf8a1-7432-46c3-9dc9-781f48edb3e1.png">

<img width="1007" alt="Screenshot 2023-01-26 at 23 27 33" src="https://user-images.githubusercontent.com/90892301/214957694-bf6ff2ef-d76e-427b-a375-dd12728869e4.png">

+ General: Developer tools

<img width="1022" alt="Screenshot 2023-01-26 at 23 29 15" src="https://user-images.githubusercontent.com/90892301/214957825-c866fb56-621c-4b9d-88c3-abe206ba73a0.png">

<img width="1013" alt="Screenshot 2023-01-26 at 23 42 21" src="https://user-images.githubusercontent.com/90892301/214957882-c990daeb-b108-4681-8898-b6a0cff7ceb4.png">

In the end, I managed to complete the required exercises and find the answers to the questions offered in the "HTML Basics" and "Developer tools". 



