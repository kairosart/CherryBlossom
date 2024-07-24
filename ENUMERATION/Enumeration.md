## Services and ports
```
nmap -A 10.10.X.X
```

![[Enumeration-20240716133325591.webp]]

The OS is Linux.
Open ports are: 22, 139 and 445. Three open ports, all standard. 
- SSH running on Port 22 — there’s nothing you can do with this for now; not without at least a username. 
- (139 and 445) are both for Samba. 

## Samba fileshare
The first thing we need to do is enumerate the Samba fileshare to see if there’s anything you can make use of. Run another nmap scan, this time using the `smb-enum-shares` script:

```
nmap --script smb-enum-shares -vv <remote-ip>
```

![[Enumeration-20240716135707781.webp]]

**Next step :** [[Samba access]]
