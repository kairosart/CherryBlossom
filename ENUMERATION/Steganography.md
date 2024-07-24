Steganography is the practice of concealing messages or information within other non-secret text or data. The term comes from the Greek words "steganos" (meaning covered or concealed) and "graphein" (meaning writing). Unlike cryptography, which obscures the content of a message, steganography hides the very existence of the message.

## Stegpy
To extract the data from the journal_image.png use a tool called [stegpy](https://github.com/dhsdshdhk/stegpy). 

- Install it using `pip3 install stegpy`.

	![[Samba access-20240522141535584.webp]]

- Extract the file:
```
	$ /home/kali/.local/bin/stegpy journal_image.png
```

File journal.zip succesfully extracted from journal_image.png

The file extracted is **journal.zip**.

**Next step:** [[Journal.zip]]

