# Level 5

We have a new folder here named **".trash"** that contains a binary called **"bin"**. running it will give as a list of **0**s and **1**s groupped 8 by 8 which is the way **ASCII** characters are represented in binary. So I made a quick python script to convert it.

```python
password = "00110000 01100100 01111001 01111000 01010100 00110111 01000110 00110100 01010001 01000100 00001010".split()
password = [int(byte,2) for byte in password]
password = [chr(byte) for byte in password]
print(''.join(password))
```

Running this code will provide us the password for the next level.