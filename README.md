# Ecploit-kernel-4.10-linux-local
Linux kernel &lt; 4.10.15 - Race Condition Privilege Escalation
Linux kernel < 4.10.15
CVE-2017-1000112
This is a proof-of-concept local root exploit for the vulnerability in the UFO Linux kernel implementation CVE-2017-1000112.

Some details: http://www.openwall.com/lists/oss-security/2017/08/13/1

s/timerfd.c Vulnerbility Exploit
Vulnerable: Kernal
Google Android 0
Debian Linux 6.0 sparc
Debian Linux 6.0 s/390
Debian Linux 6.0 powerpc
Debian Linux 6.0 mips
Debian Linux 6.0 ia-64
Debian Linux 6.0 ia-32
Debian Linux 6.0 arm
Debian Linux 6.0 amd64
http://ricklarabee.blogspot.com.tr/2017/12/adapting-poc-for-cve-2017-1000112-to.html
EXPLOIT
https://github.com/xairy/kernel-exploits/tree/master/CVE-2017-1000112
// user@ubuntu:~$ uname -a
// Linux ubuntu 4.8.0-58-generic #63~16.04.1-Ubuntu SMP Mon Jun 26 18:08:51 UTC 2017 x86_64 x86_64 x86_64 GNU/Linux

// user@ubuntu:~$ id
// uid=1000(user) gid=1000(user) groups=1000(user),4(adm),24(cdrom),27(sudo),30(dip),46(plugdev),113(lpadmin),128(sambashare)

// user@ubuntu:~$ gcc pwn.c -o pwn
// user@ubuntu:~$ ./pwn
// user@ubuntu:/home/user# id
// uid=0(root) gid=0(root) groups=0(root)
https://www.exploit-db.com/exploits/41994/
Linux Kernel 4.8.0-41-generic (Ubuntu)

Exploit :
https://github.com/xairy/kernel-exploits/blob/master/CVE-2017-7308/poc.c
// user@ubuntu:~$ uname -a
// Linux ubuntu 4.8.0-41-generic #44~16.04.1-Ubuntu SMP Fri Mar 3 ...
// user@ubuntu:~$ gcc pwn.c -o pwn
// user@ubuntu:~$ ./pwn
// user@ubuntu:/home/user# id
// uid=0(root) gid=0(root) groups=0(root)
https://www.exploit-db.com/exploits/41994/
Linux Kernel 4.4.0 (Ubuntu) - DCCP Double-Free (PoC)
Includes a semireliable SMAP/SMEP bypass.

Exploit :
https://github.com/xairy/kernel-exploits/blob/master/CVE-2017-6074/poc.c
// Usage:
// $ gcc poc.c -o pwn
// $ ./pwn
// # cat /etc/shadow
// ...
// daemon:*:17149:0:99999:7:::
// bin:*:17149:0:99999:7:::
// sys:*:17149:0:99999:7:::
// sync:*:17149:0:99999:7:::
// games:*:17149:0:99999:7:::
______________________
https://www.exploit-db.com/exploits/41995/
Linux Kernel 3.11 < 4.8 0 - 'SO_SNDBUFFORCE'

Exploit :
https://github.com/xairy/kernel-exploits/blob/master/CVE-2016-9793/poc.c
// Usage:
// # gcc -pthread exploit.c -o exploit
// # chown guest:guest exploit
// # setcap cap_net_admin+ep ./exploit
// # su guest
// $ whoami
// guest
// $ ./exploit
// # whoami
// root
