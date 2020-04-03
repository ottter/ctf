<h4> Given a log file (or two) with long list of entries in this format:</h4>

```
2017-01-02 08:37:15 [Alfredo Carter] Swipe In
2017-01-02 08:39:39 [Yvette Wiegand] Swipe In
2017-01-02 08:45:46 [Amya Lebsack] Swipe In

2017-01-02 09:24:54 [Kaia Hegmann] Access 44.185.152.215 - 73913KB
2017-01-02 09:26:24 [Kaia Hegmann] Access 22.128.98.72 - 44461KB
2017-01-02 09:26:51 [Sammy Klein] Access 130.231.134.63 - 13591KB
```

<h5>Find number of unique names</h5>
```
# cut -d [ -f 2 badge.log | cut -d ] -f 1 | cat > output.txt
# cut -d [ -f 2 access.log | cut -d ] -f 1 | cat >> output.txt
# sort output.txt | uniq -c
# sort output.txt | uniq | wc -l
```
`cut -d _ -f _` will cut each line at the specific delimiter and select the field to keep<br>
`uniq -c` will display all of the values with the number of times they show up<br>
`wc -l` will display the number of lines

<h5>Separate and sum the KB in the log file</h5>
```
# cut -d - -f 4 access.log | cut -d K -f 1 | cat > output.txt
# sudo apt-get install num-utils
# numsum output.txt
```

<h5>Find number of unique IP addresses</h5>
```
# grep -E -o "([0-9]{1,3}[\.]){3}[0-9]{1,3}" input > output.txt
# sort output.txt | uniq | wc -l
```