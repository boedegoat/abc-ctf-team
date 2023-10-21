
#### information-wu

Files can always be changed in a secret way. Can you find the flag? [cat.jpg](https://mercury.picoctf.net/static/e5825f58ef798fdd1af3f6013592a971/cat.jpg)
	wu:
	first i wanted to find what file it is
	![image](https://github.com/boedegoat/abc-ctf-team/assets/141028569/29749641-2a6b-4b2e-9057-ea734c27cec9)
	ok its a jpeg file does it have a secret file inside it lets check it out at binwalk
	![image](https://github.com/boedegoat/abc-ctf-team/assets/141028569/1a082a3f-efcd-4800-a87c-f7000b1055ed)
	ok it doesnt look like it has a secret file, lets look at strings
	![image](https://github.com/boedegoat/abc-ctf-team/assets/141028569/a0083dbd-5d4a-44bf-a094-98aee0e72e91)
	nothing too lets check with exif tool then 
	![image](https://github.com/boedegoat/abc-ctf-team/assets/141028569/8525a69a-40fb-40bd-855f-0bf1ce536ca3)
	ok i see something interesting in the license category could be base64?
	![image](https://github.com/boedegoat/abc-ctf-team/assets/141028569/3bec1ca0-fb93-4200-b350-21c0ab8055fd)
	ok then we get the flag
	picoCTF{the_m3tadata_1s_modified}
