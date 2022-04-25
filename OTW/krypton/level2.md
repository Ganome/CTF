This flag was stored using the same ROT13 cypher as the bandit level.

Using the same sed string as before:

This file is not in the home directory - find it using the "find / -iname krypton2 2>/dev/null" command

krypton1@krypton:/krypton/krypton1$ cat krypton2
YRIRY GJB CNFFJBEQ EBGGRA
krypton1@krypton:/krypton/krypton1$ sed y/abcdefghijklmnopqrstuvwxyzABCDEFGHIJKLMNOPQRSTUVWXYZ/nopqrstuvwxyzabcdefghijklmNOPQRSTUVWXYZABCDEFGHIJKLM/ /krypton/krypton1/krypton2
LEVEL TWO PASSWORD ROTTEN
