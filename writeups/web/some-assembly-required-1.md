---
description: 'Author: boedegoat'
---

# Some Assembly Required 1

<figure><img src="../../.gitbook/assets/image (30).png" alt=""><figcaption><p><a href="https://play.picoctf.org/practice/challenge/152?category=1&#x26;page=1">https://play.picoctf.org/practice/challenge/152?category=1&#x26;page=1</a></p></figcaption></figure>

First open the given link [http://mercury.picoctf.net:37669/index.html](http://mercury.picoctf.net:37669/index.html). There is no interesting thing on the page. From the challenge title, It's giving us a clue that we need to find assembly code. So, I opened up the firefox debugger tab and I found `wasm://` folder. Inside of it, there is a file but when I try to opened It says "Please refresh to debug this module". Then I refresh it, opened the file again, and just scroll down to the bottom.

<figure><img src="../../.gitbook/assets/image (32).png" alt=""><figcaption></figcaption></figure>

🎉 That's it, we got the flag `picoCTF{XML_3xtern@l_3nt1t1ty_e5f02dbf}`
