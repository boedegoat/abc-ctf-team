---
description: 'Author: Ey3s'
---

# Matryoshka-wu

Matryoshka dolls are a set of wooden dolls of decreasing size placed one inside another. What's the final one? Image: [this](https://mercury.picoctf.net/static/b6205dd933ec01c022c4e6acbdf11116/dolls.jpg)

we can instantly use binwalk on this with the matryoshka flag (-M)

<figure><img src="../../../../.gitbook/assets/image (6).png" alt=""><figcaption></figcaption></figure>

at the last extract we can see the end point of it that has a flag.txt in it so all we can do is just cd into the directories and open the text file and at last we will have the flag

picoCTF{ac0072c423ee13bfc0b166af72e25b61}
