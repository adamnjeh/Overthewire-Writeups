# Level 3

Continuing with **Caser cipher**, this time we have a binary that does the encryption for us with key saved in the file **keyfile.dat** and of course we can't open it. So what we can do is running the program on a file that contains the letter **"A"** and see how much it shifted it. Let's follow the instructions on the **README** file :
```console
$ mktemp -d
$ cd /tmp/tmp.mRzQeHkXbi
$ ln -s /krypton/krypton2/keyfile.dat 
$ chmod 777 .
$ echo A > plain.txt
$ /krypton/krypton2/encrypt plain.txt 
$ ls
$ cat ciphertext
``` 
And the output is the letter **"M"** so it shifter it with 12 character. To revert it, we need to shift the ciphered text 14 characters forward (12 + 14 = 26 which is the number of teh alphabet letters). So the next command will do the trick.

```console
$ cat /krypton/krypton2/krypton3 | tr 'A-Z' 'O-ZA-P'
```