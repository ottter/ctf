# MGA CTF 2020 – Tricky Shifty

* **Category:** Cryptography
* **Points:** 450

## Challenge

> We intercepted this message "team I will contact you with an ENCODED message just remember to SHIFT your 
clock by 14 minutes and remember to add 1 + 2 + 3 + 4 1uoqdt{cvwtdKN4zj}". See if you can decode the flag.

## Solution

This one took me a while to get even though in hindsight the prompt was right in front of me. Take the alphabet and 
add 1234 to the end of it and [Caesar shift](https://www.dcode.fr/caesar-cipher) it. I'm honestly a little bit
embarassed it took me this long.

```
import string

letters = list(string.ascii_lowercase + '1' + '2' + '3' + '4')
cipher = '1uoqdtcvwtdkn4zj'

key = []
for ciph in cipher:
	position = letters.index(ciph)
	key.append(letters[position-14])
print(key)
```

I did it by hand at first and got the wrong answer because I used lower and upper case alphabet, which completely
changed the result because of the `1234` at the end. Oh well.

```
mgactf{shift14plz}
```