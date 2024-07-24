You can’t, by default, crack 7zip files in John or Hashcat.  
You’re going to need a couple of extra libraries before we can do that. Run this commands to install them:

```
$ sudo apt update && sudo apt install lzma && sudo apt install liblzma-dev

$ wget https://cpan.metacpan.org/authors/id/P/PM/PMQS/Compress-Raw-Lzma-2.093.tar.gz

$ tar -xvzf Compress-Raw-Lzma-2.093.tar.gz && cd Compress-Raw-Lzma-2.093

$ cd Compress-Raw-Lzma-2.093
$ sudo perl Makefile.PL && sudo make && sudo make test && sudo make install
```

## Getting hash with 7z2john.pl

You should now be able to use a script called `7z2john.pl` that comes with John-the-Ripper. It’s often not located in your PATH, so it’s well worth doing `locate 7z2john` in order to find it first.

Run:

```
/usr/share/john/7z2john.pl <path-to-journal.ctz> > hash
```


## Breaking the password with John-the-Ripper

```
john --wordlist=<path-to-rockyou> <path-to-hash>
```

![[Cracking a 7zip file-20240717140639131.webp]]
The password is: **tigerlily**

**Next step:** [[Opening the journal.ctz file (Journal flag)]]