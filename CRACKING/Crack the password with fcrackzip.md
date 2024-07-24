If you don’t already have `frackzip` installed, you can get it easily on Kali by using the command: `sudo apt-get install fcrackzip`.
```
$ fcrackzip -uDp /usr/share/wordlists/rockyou.txt journal.zip
```

PASSWORD FOUND!!!!: pw == september

- Unzip the file.
```
$ unzip journal.zip 

```

![[Samba access-20240522144335027.webp]]

**CherryTree** is a powerful, feature-rich note-taking and organizing application. It's an open-source hierarchical note-taking application, featuring rich text and syntax highlighting, storing data in a single XML or SQLite file.

A `.ctz` file is an encrypted Cherrytree document. If you use `file` on this document, it will tell you that this is actually a 7zip file, because that’s how Cherrytree saves its encrypted documents.

**Next step:** [[Cracking a 7zip file]]
