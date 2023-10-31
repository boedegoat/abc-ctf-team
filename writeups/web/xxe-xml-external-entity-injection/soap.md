---
description: 'Author: Bhremada Fevreano'
---

# SOAP

<figure><img src="../../../.gitbook/assets/image (14).png" alt=""><figcaption><p><a href="https://play.picoctf.org/practice/challenge/376?category=1&#x26;page=2">https://play.picoctf.org/practice/challenge/376?category=1&#x26;page=2</a></p></figcaption></figure>

From opening the sources code in firefox debugger, I got two javascript files

<figure><img src="../../../.gitbook/assets/image (25).png" alt=""><figcaption></figcaption></figure>

It seems we can inject XML script inside there.

<figure><img src="../../../.gitbook/assets/image (24).png" alt=""><figcaption></figcaption></figure>

Also, take a look at that first 6 lines of code. Basically, we need to find element with a classname `.detailForm` in order to perform our XML injection.

<figure><img src="../../../.gitbook/assets/image (26).png" alt=""><figcaption></figcaption></figure>

Got it. It turns out the Details buttons are our gateway to get the flag. Without any further a do, let's spin up burpsuite to capture the request on clicking Details button.

<figure><img src="../../../.gitbook/assets/image (27).png" alt=""><figcaption></figcaption></figure>

Alright, it sends XML as payload. Let's inject it to read `/etc/passwd`

After some googling, I got really nice example of the injection from [PortSwigger](https://portswigger.net/web-security/xxe)

<figure><img src="../../../.gitbook/assets/image (28).png" alt=""><figcaption></figcaption></figure>

Let's implemented it to our http request payload

<figure><img src="../../../.gitbook/assets/image (29).png" alt=""><figcaption></figcaption></figure>

🎉 And that's it, we got the flag `picoCTF{XML_3xtern@l_3nt1t1ty_e5f02dbf}`
