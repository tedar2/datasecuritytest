# Report h01

![HH Logo](https://github.com/tedar2/datasecuritytest/blob/b06717bd3ba1f566c179f3dc5952aa4f8ee270b7/HH%20logo.png) 

### task z)

### Hutchins et al 2011: Intelligence-Driven Computer Network Defense Informed by Analysis of Adversary Campaigns and Intrusion Kill Chains (summary)

#### Intro

+ a new class of threats emerged - "Advanced Persistent Threat" or APT 
+ conventional incident response methods fail to mitigate the risk with APT intrusions
+ APT actors continually demonstrate the capability to compromise systems by using advanced tools, customized malware, and "zero-day" exploits that anti-virus and patching cannot detect or mitigate
+ responses to APT intrusions reqiure an evolutions in analysis, process and technology
+ intelligence-driven, threat focused approach to study intrusions from the adversaries' perspective
+ each discrete phase is mapped to one step - detection, mitigation and response
+ "kill chain" - describes the structure of intrusion; throuhg this model, defenders can develop resilient mitigations against intruders 
+ "kill chain" (U.S. Department of Defence, 2007) stages are fix, track, target, engage, access

#### Chapter 3.2 and 3.3 

+ a kill chain is a systematic process to target and engage an adversary to create desired effects
+ steps are find, fix, track, target, engage, assess (F2T2EA)
+ a new kill chain model, developed specifically for intrusions: the agressor must develop a payload ro breach a trusted boundary, establish a presence inside a trusted environment, and from that presence, take actions towards their objectives
+ the intrusion kill chain: Reconnaisance, Weaponization, Delivery, Exploitation, Installation, Command and Control (C2), Actions on Objectives
+ courses of Action Matrix: 

![](https://github.com/tedar2/datasecuritytest/blob/c44e2d4c87cb1401f2752057fbd69432d4358340/Screenshot%202023-01-22%20at%2019.47.49.png)

+ Defenders can generate metrics of the resiliency by measuring the performance and effectiveness of defensive actions against intruders


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

### a) Bandit oh-five exercizes. I was not sure if I can list the commands and&or passwords here to avoid spoilers, but I attach some screenshots of the levels:

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

### b) Install Debian

My setup differs a bit as I find the best app to work with on MacPro with the M1 core is Parallels so far - 

<img width="634" alt="image" src="https://user-images.githubusercontent.com/90892301/214112185-5f16f8c9-d1dd-4bd9-ac26-b2256691921c.png">




