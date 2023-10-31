---
description: 'Author: boedegoat'
---

# Web Gauntlet

### Problem

Can you beat the filters? Log in as admin [http://jupiter.challenges.picoctf.org:40791/](http://jupiter.challenges.picoctf.org:40791/) [http://jupiter.challenges.picoctf.org:40791/filter.php](http://jupiter.challenges.picoctf.org:40791/filter.php)

### Solution

<figure><img src="../../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

Alright, let's play with sql injection. FIrst, I try to input `admin` as username and password, and of course it's wrong. Then, I input `admin' --` as username and leave random password.

<figure><img src="../../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

Let's keep goin'. In second round, seems like I can't use `--` anymore

<figure><img src="../../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

Well, there are other ways to comments in sql. So I try to input `admin' /*`

<figure><img src="../../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

In 3th round, I do the same way because the filter still not filtering `/*`

<figure><img src="../../../.gitbook/assets/image (4).png" alt=""><figcaption></figcaption></figure>

In 4th round, things start to be interesting. I can't use `admin` anymore because it's filtered.

<figure><img src="../../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

So I use `||` to construct 'admin' by concatenate it: `ad'||'min'/*`

<figure><img src="../../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

In 5th round, I use `ad'||'min';` just for ~~fun~~ variation.

<figure><img src="../../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

Finally, I can grab the flag

<figure><img src="../../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

Flag: `picoCTF{y0u_m4d3_1t_96486d415c04a1abbbcf3a2ebe1f4d02}`

