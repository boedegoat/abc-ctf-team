---
description: 'Creator: Bhremada Fevreano'
---

# GET aHead

<figure><img src="../../.gitbook/assets/image.png" alt=""><figcaption></figcaption></figure>

first we need to open the given website link: [http://mercury.picoctf.net:45028/](http://mercury.picoctf.net:45028/)

<figure><img src="../../.gitbook/assets/image (1).png" alt=""><figcaption></figcaption></figure>

Nothing interesting here, that two buttons are just for changing the website background color. Let's use burpsuite to intercept the http request.

Here's the request when I click Choose Red button

<figure><img src="../../.gitbook/assets/image (2).png" alt=""><figcaption></figcaption></figure>

And here's the request when I click Choose Blue button

<figure><img src="../../.gitbook/assets/image (3).png" alt=""><figcaption></figcaption></figure>

As you can see, Choose Red button makes a GET request, and Choose Blue button makes a POST request.&#x20;

From the first hint, it says "Maybe you have more than 2 choices". So I look up for another HTTP methods other than GET and POST.

<figure><img src="../../.gitbook/assets/image (4).png" alt=""><figcaption><p>source: <a href="https://computernetworkingsimplified.wordpress.com/tag/http-methods/">https://computernetworkingsimplified.wordpress.com/tag/http-methods/</a></p></figcaption></figure>

If you look at there, there is a HTTP method called HEAD, and if you haven't notice, this CTF challenge title is "GET aHEAD". So let's try to send HTTP request by using HEAD method.

<figure><img src="../../.gitbook/assets/image (5).png" alt=""><figcaption></figcaption></figure>

And that's it, we got the flag `picoCTF{r3j3ct_th3_du4l1ty_775f2530}`
