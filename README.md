# CTF Tools README
This folder contains scripts and other files used for CTF or other cybersecurity challenges. I've compiled them all into here for ease. 

## PacketWhisper
PacketWhisper is a tool that can be used in Python to exfiltrate data through DNS queries. It's really slow (15 minutes for 800 bytes) but very stealthy. It must be on the target's computer in order to work, and you must be capturing the network traffic as it transmits. 

## EgressCheck Framework
This python script can be used to generate python commands used on the target device to check which outgoing ports are allowed. For example, let's say I want to exfiltrate data from Comp1, and my computer is Comp2, I can run this script on Comp2, specify the target and source IP, and then run `generate python-cmd` and that will give me a base64-encoded payload in a python script. I run this command on Comp1 (which has to have Python), while also capturing traffic using tcpdump, according to the `generate tcpdump` command I also used. After it's done, I can parse the data using another command given and it will tell me which ports received data, so which ports I can access from Comp1, and use to exfiltrate data. 

## Steg_Brute
This python script is used to brute force the steghide command. It can do brute force or use a dictionary file. 

## Sublist3r and Subbrute
Sublist3r is a Python script that collects a list of possible subdomains from multiple online sources, and natively includes the subbrute script, which can be used to brute force enumerate subdomains not listed anywhere. 