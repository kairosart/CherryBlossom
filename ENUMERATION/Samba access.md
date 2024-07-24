As you saw on the enumeration section there's an anonymous account you can access without password.

```
smbclient //10.10.X.X/anonymous
```

After connecting to the samba server run:

```
smb: \> dir
```

![[Samba access-20240521151456824.webp]]

Download the file to your attaching machine.
```
smb: > get journal.txt
```

It seems a base64 file.

Decode the file:
```
 $ cat journal.txt | base64 -d > journal
 $ file journal
```

![[Samba access-20240521152526164.webp]]
It's a png file.

Copy the file with another name:

```
$ cp journal journal_image.png
```

![[Samba access-20240521153048671.webp]]

This image can have some hidden message.

**Next step:** [[Steganography]]


