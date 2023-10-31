---
description: 'Author: boedegoat'
---

# Web Gauntlet 2

### Problem

This website looks familiar... Log in as admin Site: [http://mercury.picoctf.net:46322/](http://mercury.picoctf.net:46322/) Filter: [http://mercury.picoctf.net:46322/filter.php](http://mercury.picoctf.net:46322/filter.php)

### Solution

This one is tough. The filter has improved compared to the first Web Gauntlet.

<figure><img src="../../../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

Bro, is it still possible to perform a sql injection without adding comments or semicolon? But, how about adding a poison null byte? I tried to input `ad'||'min'%00`

<figure><img src="../../../.gitbook/assets/image (11).png" alt=""><figcaption></figcaption></figure>

Wait what, it's not working. Why not to try sending login request inside burpsuite

<figure><img src="../../../.gitbook/assets/image (12).png" alt=""><figcaption></figcaption></figure>

<figure><img src="../../../.gitbook/assets/image (13).png" alt=""><figcaption></figcaption></figure>

flag: `picoCTF{0n3_m0r3_t1m3_9605a246c21764e7691ca04679ad321a}`
