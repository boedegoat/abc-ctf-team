---
description: 'Author: Ey3s'
---

# tunn3l v1s10n-wu

We found this [file](https://mercury.picoctf.net/static/7b2d7c26630e977197022d0af09e3aeb/tunn3l\_v1s10n). Recover the flag.

tbh i got a little confused on this one so i looked at the hint which says "Weird that it won't display right...", so im assuming the file is corrupt

so i opened hex editor (ps: im gonna use Hxd as my main hex editor for this wu)

<figure><img src="../../../../.gitbook/assets/image (7).png" alt=""><figcaption></figcaption></figure>

as you can see the in the decoded text the header is a bmp file's and i felt like the header needs to be worked on. and since i dont know where to start why not compare it with a fixed file so i replaced  it all and the hxd file should look like this

<figure><img src="../../../../.gitbook/assets/image (8).png" alt=""><figcaption></figcaption></figure>

the red indicates the fixed version. and after doing that i saved the file and it resulted into this picture

<figure><img src="../../../../.gitbook/assets/image (9).png" alt=""><figcaption></figcaption></figure>

alright after this i did not know what to do so after a few hours of trying to figure out i found out something this is not the maximum size so i went to kali linux and did an exiftool on the picture

<figure><img src="../../../../.gitbook/assets/image (10).png" alt=""><figcaption></figcaption></figure>

now we can see the images true max hight and width now all we need to do to bypass the height limit and width now im going to convert the height to 850  and turn it into hex which results in\
850(52 03).  now lets put it in hxd

<figure><img src="../../../../.gitbook/assets/image (16).png" alt=""><figcaption></figcaption></figure>

after that the image will turn out like this which reveals the flag!

<figure><img src="../../../../.gitbook/assets/image (18).png" alt=""><figcaption></figcaption></figure>

flag: picoCTF{qui1t3\_a\_v13w\_2020}
