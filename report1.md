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

a) Bandit oh-five exercizes.

+ bandit0 level 
<img width="571" alt="image" src="https://user-images.githubusercontent.com/90892301/214103137-b1a012c1-ef7a-4481-adce-32d989becaeb.png"> 
+ bandit1 level
<img width="262" alt="image" src="https://user-images.githubusercontent.com/90892301/214105725-9ec4e6a1-76e9-4eb8-9920-057764589192.png">

