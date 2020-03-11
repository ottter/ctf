# MGA CTF 2020 – Bronze Leader

* **Category:** Middle Georgia Wars
* **Points:** 650

## Challenge

> THIS IS SITUATION ALFA! MGSU Nuclear facility has been compromised. Vicious Bictor Hamford has surpassed all 
limits of evil and taken over the MGSU Nuclear Plant. The Bronze Squadron Leader, Dr. Wang needs your help to 
over ride the nuclear plant controls. [REDACTED LINK] use this website to access the online over ride portal. 
Unfortunately, we have not had the need to use this portal in so ling that no one knows the code to over ride 
it. Dr. Wang is certain he can get the situation under control if you get him the code. We also have information 
that there is a hidden flag on the other side for you. BUT we DO NOT have time. FIND THE CODE NOW!!

## Solution

I saw that the button on the original website checks under `GetPassInfo()` so I ctrl+f for that and found the 
correct entry to capture the flag

```
mgactf{with_no_keys_no_driving}
```