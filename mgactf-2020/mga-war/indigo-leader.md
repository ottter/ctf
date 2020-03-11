# MGA CTF 2020 – Indigo Leader

* **Category:** Middle Georgia Wars
* **Points:** 650

## Challenge

> Indigo Squadron Leader, Dr. Kwak has had success in obtaining a crucial code used by Middle Georgia Pirate 
Company. Although, Indigo Leader has since been busy and has not been able to to do much with the code. 
Please find the hidden flag. What is the Flag?

## Solution

The contents of the Ruby file had these lines:
```
flag = [95, 85, 83, 81, 70, 84, 109, 117, 87, 95, 65, 109, 127, 
        83, 89, 87, 109, 107, 93, 71, 109, 96, 91, 81, 90]
a.chars.map { |c, i| c.unpack("U*")[0] ^ 50 == flag[i] }
```

I uninstalled Ruby from my computer probably a week prior to this competition so instead of trying to make
this run properly, I reverse engineered it with a quick Python script. Future, lazy me is going to be annoyed that
I didn't post that here.

```
mgactf{Gems_Make_You_Rich}
```