# MGA CTF 2020 – Decoding #2

* **Category:** Cryptography
* **Points:** 80

## Challenge

> A group of hackers have been working to set up a meeting. See if you can decode their usernames. 
Hacker 2 - 34 4c 69 74 74 6c 65 4e 69 63 6b 79 31 31

## Solution

Hexadecimal (base16) uses the characters `0-9` and `a-f`. Noticing for that, along with the added spacing, is a good
sign to check if a code is encoded in hex.

[Cyber Chef](https://gchq.github.io/CyberChef/) from Hex

```
4LittleNicky11
```