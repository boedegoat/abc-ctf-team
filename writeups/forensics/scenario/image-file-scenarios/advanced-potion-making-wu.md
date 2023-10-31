---
description: 'Author: Ey3s'
---

# advanced-potion-making-wu

Ron just found his own copy of advanced potion making, but its been corrupted by some kind of spell. Help him recover it!



in this challenge there are no hints so i just wondered for a few minutes on how to do this so the first thing i check is the file type&#x20;

<figure><img src="../../../../.gitbook/assets/image (1) (1).png" alt=""><figcaption></figcaption></figure>

low and behold its a data type. ok then i pulled up my hex editor and i found that the file was corrupted how did i know that? lets see this picture below

<figure><img src="../../../../.gitbook/assets/image (1) (1) (1).png" alt=""><figcaption></figcaption></figure>

the image above shows that its a corrupted png you can see by the header, ihdr, srgb, and gama. next thing i did was i fixed the file by comparing it to another working img

<figure><img src="../../../../.gitbook/assets/image (3) (1).png" alt=""><figcaption></figcaption></figure>

now that i fixed it, i saved it and renamed it to .png, and the result of the fixed data is below



<figure><img src="../../../../.gitbook/assets/advanced-potion-making (1) (1).png" alt=""><figcaption></figcaption></figure>



ok what can i do with this you might ask, next thing to do is upload it to apperi's solve or any steganography tool you have

thus, we have uncovered the flag!

<figure><img src="../../../../.gitbook/assets/image (5) (1).png" alt=""><figcaption></figcaption></figure>

flag: picoCTF{w1z4rdry}
