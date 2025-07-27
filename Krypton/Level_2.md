# Level 2

Let's go to **/krypton/krypton1/** folder. According to the **"README"** file, the password is encrypted in the file **"krypton2"** using **ROT13** which is also know as **Caesar Cyphering** and what it does is shifting each character with 13 step on an alphabet cycle : A --> N; B --> O; C --> P; ...

We can solve this using **tr** command which transform characters to other accoridng a choosen pattern

```console
$ cat krypton2 | tr 'A-Za-z' 'N-ZA-Mn-za-m'
```
where **'A-Z'** represent the alphabet list in uppercase, **'a-z'** the alphabet list in lowercase, **'A-Za-z'** concatinating the previous two lists, **'N-ZA-M'** the alphabet in uppercase rotated by 13 to strat from "N" and end in "M", **'n-za-m'** the alphabet in lowercase rotated by 13 to strat from "n" and end in "m" and **'N-ZA-Mn-za-m'** concatinating the previous two lists.