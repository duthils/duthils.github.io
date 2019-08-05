# Diagnostic and repair of an OpenSUSE system

## It's broken! Help!

- Hey my laptop is not working anymore!
- Hum... What do you see?
- A black screen!
- OK I'm coming.

And there it is... the Linux Black Screen of Death... Kernel panic!

- That's not black! At least it's talking!
- Yeah, talking yiddish... 
- What happened?
- I upgraded the system and when I restarted the computer, it started talking gibberish.

So... The new Linux kernel crashes when the system is loading.

First thing to try: try another version of the kernel.

TO BE CONTINUED...

In short:
```
rpm
> symbol getxattr version ATTR_1.0 not defined in file libattr.so.1 with link time reference
zypper

rpm2cpio /mnt/var/cache/zypp/packages/http-download.opensuse.org-c9fdbd26/x86_64/libattr1-2.4.48-2.8.x86_64.rpm | cpio -idmv
http://download.opensuse.org/distribution/leap/15.1/repo/oss/x86_64/
rpm2cpio /tmp/libattr1-2.4.47-lp151.3.70.x86_64.rpm | cpio -idmv

mint:/ # cat /etc/zypp/repos.d/http-download.opensuse.org-*
[http-download.opensuse.org-84f1799f]
name=home:medozas74
enabled=1
autorefresh=1
baseurl=http://download.opensuse.org/repositories/home:/medozas74/openSUSE_Leap_15.0/
type=rpm-md
keeppackages=0
[http-download.opensuse.org-c9fdbd26]
name=openSUSE:Factory
enabled=1
autorefresh=1
baseurl=http://download.opensuse.org/tumbleweed/repo/oss/
type=rpm-md
keeppackages=0

sudo rpm -ivh --force --noscripts --root=/mnt libattr1-2.4.47-lp151.3.70.x86_64.rpm

mint:/ # ls -l /lib64/libattr*
lrwxrwxrwx 1 root root    16 May 12  2018 /lib64/libattr.so.1 -> libattr.so.1.1.0
-rw-r--r-- 1 root root 18824 May 12  2018 /lib64/libattr.so.1.1.0

mint:/ # ls -l /usr/lib64/libattr*
...

ln -nsf /lib64/libattr.so.1 /usr/lib64/libattr.so.1
zypper

mv /etc/zypp/repos.d/http-download.opensuse.org-c9fdbd26.repo{,.disabled.tumbleweed}

zypper dup
zypper addlock texlive-*
zypper dup
```
