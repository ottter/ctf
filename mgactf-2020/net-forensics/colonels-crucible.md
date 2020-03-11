# MGA CTF 2020 – Colonel's Crucible

* **Category:** Network Forensics
* **Points:** 600 / 800 / 1000

## Challenge

> Welcome to the Colonel’s Crucible. Only the bravest of cyber warriors dare inter. Within this category you 
will face three challenges with increasing difficulty. These challenges will test your perseverance, critical 
thinking, and cyber-skills. Good luck. Your first challenge: Someone exfiltrated a flag from our network. I’ve 
isolated the suspicious packets to make your job easier. Find the exfiltrated flag and submit it as your answer.

## Solution

I was only able to solve the first flag in time. In the .pcap file, if you went packet by packet and converted the 
port destination from decimal to ASCII, the flag is right there.

```
mgactf{Ashubbery501}
```