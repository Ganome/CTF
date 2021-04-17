leviathan3@leviathan:~$ ltrace ./level3
__libc_start_main(0x8048618, 1, 0xffffd784, 0x80486d0 <unfinished ...>
strcmp("h0no33", "kakaka")                              = -1
printf("Enter the password> ")                          = 20
fgets(Enter the password> AAAA
"AAAA\n", 256, 0xf7fc55a0)                        = 0xffffd590
strcmp("AAAA\n", "snlprintf\n")                         = -1
puts("bzzzzzzzzap. WRONG"bzzzzzzzzap. WRONG
)                              = 19
+++ exited (status 0) +++

************We can see that its using the strcmp() function, and looking for the string "snlprintf"   Let's try that

leviathan3@leviathan:~$ ./level3
Enter the password> snlprintf
[You've got shell]!
$ whoami
leviathan4
$ cat /etc/leviathan_pass/leviathan4
vuH0coox6m