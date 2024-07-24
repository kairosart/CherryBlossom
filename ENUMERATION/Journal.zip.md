- Unzip the _journal.zip.
```
$ unzip _journal.zip
```

![[Journal.zip-20240716143923533.webp]]

That error looks like the archive has been corrupted somehow. Let’s try using `file` on it to see if it actually _is_ a zip archive:

```
file _journal.zip
```

![[Samba access-20240522142815194.webp]]

it’s a JPEG file

- Convert this jpeg into a zip file. You have to change the headers to something like 50 4B 03 04.
```
$ hexeditor _journal.zip
```

![[hexeditor.png]]

If you try to unzip it you'll see you need a password.

**Next step :** [[Crack the password with fcrackzip]]
