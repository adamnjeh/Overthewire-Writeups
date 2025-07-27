# Level 1

The level description gave us the strings **"S1JZUFRPTklTR1JFQVQ="** and told us it is **base64** encoded (which is not that hard to guess)

A simple command will do the trick for us

```console
$ echo "S1JZUFRPTklTR1JFQVQ=" | base64 -d
```