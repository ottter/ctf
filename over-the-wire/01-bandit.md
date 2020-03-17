# OverTheWire - Level 1

login:`bandit[level]`<br>
pass:`[pass]`

### Bandit

<h6>Level 00 > 01:</h6>
```commandline
bandit0@bandit:~$ ls
readme
bandit0@bandit:~$ cat readme
boJ9jbbUNNfktd78OOpsqOltutMc3MY1
```
<h6>Level 01 > 02:</h6>
```commandline
bandit1@bandit:~$ ls
-
bandit1@bandit:~$ cd -
-bash: cd: OLDPWD not set
bandit1@bandit:~$ cat ./-
CV1DtqXWVFXTvM2F0k09SHz0YwRINYA9
```
<h6>Level 02 > 03:</h6> 
```commandline
bandit2@bandit:~$ ls
spaces in this filename
bandit2@bandit:~$ cat spaces\ in\ this\ filename
UmHadQclWmgdLOKQ3YNgjWxGoRMb5luK
```
<h6>Level 03 > 04:</h6>
```commandline
bandit3@bandit:~$ ls
inhere
bandit3@bandit:~$ cd inhere/
bandit3@bandit:~/inhere$ ls
bandit3@bandit:~/inhere$ ls -a
.  ..  .hidden
bandit3@bandit:~/inhere$ cat .hidden
pIwrPrtPN36QITSp3EQaw936yaFoFgAB
```

<h6>Level 04 > 05:</h6>
```commandline
bandit4@bandit:~$ ls
inhere
bandit4@bandit:~$ cd inhere/
bandit4@bandit:~/inhere$ ls
-file00  -file02  -file04  -file06  -file08
-file01  -file03  -file05  -file07  -file09
bandit4@bandit:~/inhere$ find . -type f -exec cat {} +
N▒{▒▒Y▒d4▒▒▒]3▒▒▒▒▒9(▒
Q▒▒▒▒▒@▒%@▒▒▒ZP*E▒▒1▒V▒▒▒̫*▒▒▒ۻ▒▒U"7▒w▒▒▒H▒▒ê▒Q▒▒(▒▒▒#▒▒▒▒T▒v▒▒(▒ִ▒▒▒▒▒A*▒
2J▒Ş؇_▒y7+▒▒pm▒▒▒;▒▒:D▒▒^▒▒@▒gl▒Q▒▒.A▒▒u▒▒#▒▒▒w$N?c▒-▒▒Db3▒▒=▒▒FPn▒
                                                                   '▒U▒▒▒M▒▒/u
XS
▒mu▒z▒▒▒хkoReBOKuIDDepwhWk7jZC0RTdopnAYKh
▒=<▒W▒▒▒▒▒ht▒Z▒▒!▒▒{▒U
▒▒▒▒▒▒~%        C[▒걱>▒▒| ▒
```   
Note: `x` at start is not part of the password
<h6>Level 05 > 06:</h6>
```commandline
bandit5@bandit:~$ ls
inhere
bandit5@bandit:~$ cd inhere/
bandit5@bandit:~/inhere$ ls -a
.            maybehere02  maybehere06  maybehere10  maybehere14  maybehere18
..           maybehere03  maybehere07  maybehere11  maybehere15  maybehere19
maybehere00  maybehere04  maybehere08  maybehere12  maybehere16
maybehere01  maybehere05  maybehere09  maybehere13  maybehere17
bandit5@bandit:~/inhere$ find . -type f ! -executable -size 1033c
./maybehere07/.file2
bandit5@bandit:~/inhere$ cat ./maybehere07/.file2
DXjZPULLxYr17uwoI01bNLQbtFemEgo7
```
<h6>Level 06 > 07:</h6>
```commandline
bandit6@bandit:~$ ls
bandit6@bandit:~$ ls -a
.  ..  .bash_logout  .bashrc  .profile
bandit6@bandit:~$ find / -user bandit7 -group bandit6 -size 33c
find: ‘/run/screen/S-bandit5’: Permission denied
find: ‘/run/screen/S-bandit17’: Permission denied
/var/lib/dpkg/info/bandit7.password
find: ‘/var/lib/apt/lists/partial’: Permission denied
find: ‘/var/lib/polkit-1’: Permission denied
bandit6@bandit:~$ cat /var/lib/dpkg/info/bandit7.password
HKBPTKQnIay4Fw76bEy8PVxKEDQRKTzs
```
<h6>Level 07 > 08:</h6> 
```commandline
bandit7@bandit:~$ ls
data.txt
bandit7@bandit:~$ cat data.txt | grep "millionth"
millionth       cvX2JJa4CFALtqS87jk27qwqGhBM9plV
```
<h6>Level 08 > 09:</h6>
```commandline
bandit8@bandit:~$ ls
data.txt
bandit8@bandit:~$ sort data.txt | uniq -u
UsvVyFSfZZWbi6wgC7dAFyFuR6jQQUhR
```
<h6>Level 09 > 10:</h6>
```commandline
bandit9@bandit:~$ ls
data.txt
bandit9@bandit:~$ strings data.txt | grep "==="
2========== the
========== password
========== isa
========== truKLdjsbJ5g7yyJ2X2R0o3a5HQJFuLk
```

<h6>Level 10 > 11:</h6> 
```commandline
bandit10@bandit:~$ ls
data.txt
bandit10@bandit:~$ cat data.txt
VGhlIHBhc3N3b3JkIGlzIElGdWt3S0dzRlc4TU9xM0lSRnFyeEUxaHhUTkViVVBSCg==
bandit10@bandit:~$ ^C
bandit10@bandit:~$ VGhlIHBhc3N3b3JkIGlzIElGdWt3S0dzRlc4TU9xM0lSRnFyeEUxaHhUTkViVVBSCg== | base64 -d
bandit10@bandit:~$ echo !!
echo VGhlIHBhc3N3b3JkIGlzIElGdWt3S0dzRlc4TU9xM0lSRnFyeEUxaHhUTkViVVBSCg== | base64 -d
The password is IFukwKGsFW8MOq3IRFqrxE1hxTNEbUPR
```
<h6>Level 11 > 12:</h6> 
```commandline
bandit11@bandit:~$ cat data.txt
Gur cnffjbeq vf 5Gr8L4qetPEsPk8htqjhRK8XSP6x2RHh
bandit11@bandit:~$ cat data.txt | tr '[a-z]' '[n-za-m]' | tr '[A-Z]' '[N-ZA-M]'
The password is 5Te8Y4drgCRfCx8ugdwuEX8KFC6k2EUu
```
<h6>Level 12 > 13:</h6> 
```commandline

```
<h6>Level 13 > 14:</h6> 
```commandline

```
<h6>Level 14 > 15:</h6> 
```commandline

```
<h6>Level 15 > 16:</h6> 
```commandline

```
<h6>Level 16 > 17:</h6> 
```commandline

```
<h6>Level 17 > 18:</h6> 
```commandline

```
<h6>Level 18 > 19:</h6> 
```commandline

```
<h6>Level 19 > 20:</h6> 
```commandline

```