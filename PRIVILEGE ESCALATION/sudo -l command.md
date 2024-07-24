The `sudo -l` command is used to list the allowed (and forbidden) commands for the invoking user on the current host. This is useful for determining what commands you can run with `sudo` without actually executing them.

If you try sudo -l command you'll notice that you are prompted for Johan’s password, which is not unusual. What _is_ unusual is that we’re able to see asterisks as we type.

This means that there’s an activated setting called `pwfeedback` that, with vulnerable versions of sudo, will let us gain root permissions directly ([CVE-2019-18634](https://www.exploit-db.com/exploits/47995))

Due to a bug, when the pwfeedback option is enabled in the sudoers file, a user may be able to trigger a stack-based buffer overflow

Exploiting the bug does not require sudo permissions, merely that pwfeedback be enabled. 
The bug can be reproduced by passing a large input to sudo via a pipe when it prompts for a password.

    $ perl -e 'print(("A" x 100 . "\x{00}") x 50)' | sudo -S id
    Password: Segmentation fault

**Next step:** [[Exploit sudo -l vulnerability]]

