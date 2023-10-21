
#### information-wu

Files can always be changed in a secret way. Can you find the flag? [cat.jpg](https://mercury.picoctf.net/static/e5825f58ef798fdd1af3f6013592a971/cat.jpg)
	wu:
	first i wanted to find what file it is
	![[Pasted image 20231021202319.png | 800]]
	ok its a jpeg file does it have a secret file inside it lets check it out at binwalk
	![[Pasted image 20231021202450.png]]
	ok it doesnt look like it has a secret file, lets look at strings

	![[Pasted image 20231021202709.png]]
	nothing too lets check with exif tool then 
	![[Pasted image 20231021203123.png]]
	ok i see something interesting in the license category could be base64?

	![[Pasted image 20231021203323.png]]
	ok then we get the flag
	picoCTF{the_m3tadata_1s_modified}