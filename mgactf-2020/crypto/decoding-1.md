# MGA CTF 2020 – Decoding #1

* **Category:** Cryptography
* **Points:** 80

## Challenge

> A group of hackers have been working to set up a meeting. See if you can decode their usernames. 
Hacker 1 - OTlIYXBweUdpbG1vcmU4Nw==

## Solution

A code ending in `=` or `==` is a good sign to check how it converts from base64. b64 encoding adds `=` to the end
as padding, if it is required.

[Cyber Chef](https://gchq.github.io/CyberChef/) to convert from base64

```
99HappyGilmore87
```