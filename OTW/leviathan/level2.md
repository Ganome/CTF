leviathan1@leviathan:~$ ltrace ./check
__libc_start_main(0x804853b, 1, 0xffffd774, 0x8048610 <unfinished ...>
printf("password: ")                                    = 10
getchar(1, 0, 0x65766f6c, 0x646f6700password: AAAA
)                   = 65
getchar(1, 0, 0x65766f6c, 0x646f6700)                   = 65
getchar(1, 0, 0x65766f6c, 0x646f6700)                   = 65
strcmp("AAA", "sex")                                    = -1
puts("Wrong password, Good Bye ..."Wrong password, Good Bye ...
)                    = 29
+++ exited (status 0) +++
leviathan1@leviathan:~$ ./check
password: sex
$ whoami
leviathan2
$ cat /etc/leviathan_pass/leviathan2
ougahZi8Ta