# 42-Piscine-Shell00

## ex00
The `cat` command concatenates multiple files and prints their contents on the standard output. If only a single file is provided, it directly prints its content on the standard output.

## ex01
1. `truncate -s 40 testShell00`
2. `touch -t 202406012342 testShell00`
3. `chmod 455 testShell00`
3. `tar -cf testShell00.tar testShell00` (tar archive)

## ex02
1. `mkdir test0 test2`
2. `touch test1 test3 test4`
3. `ln -s test0 test6`
4. `ln test3 test5`
5. `truncate -s 4 test1; truncate -s 1 test3; truncate -s 2 test4; truncate -s 1 test5; truncate -s 5 test6`
6. `touch -t 202406012047 test0; touch -t 202406012146 test1; touch -t 202406012245 test2; touch -t 202406012344 test3; touch -t 202406012343 test4; touch -t 202406012344 test5; touch -h -d "2024-06-01 22:20:00" test6`
7. `chmod 714 test1; chmod 504 test2; chmod 404 test3; chmod 641 test4; chmod 404 test5; chmod 777 test6; chmod 715 test0`

## ex03
id_rsa_pub is the public key file generated when you create an SSH key pair using tools like ssh-keygen.
1. `ssh-keygen`
2. Press <Enter> three times.
3. `cd ~/.ssh`
4. `cat id_rsa_pub`

## ex04
Or `ls -mpt` in reverse order.

## ex05
1. Add the following two lines into your script:
   `#!/bin/bash`

   `git log --format='%H' -n5`
2. Then in your terminal, `chmod +x git_commit.sh` to grant executable permission.

Note: you can also use `git log -5 --format='%H' | cat -e`

## ex06
Other options:
`git ls-files -o -i --exclude-standard`
`git clean -Xnd | cut -b 14-256`

## ex07
1. Unpack the `resources.tar.gz` file using `tar -xvzf` if on Linux (just open it on Mac).
2. You'll find two files inside it: 'a' and 'sw.diff'.
3. The 'sw.diff' file was previously created by running the command `diff a b > sw.diff`.
4. Your job here is to re-create the 'b' file using the `patch` command.

Steps:
1. `cp a b` to duplicate/copy a new 'a' file called 'b' (to be changed).
2. `patch b < sw.diff` to patch the differences.
3. You can verify your answer by running `cat -e a` and `diff a b > test.diff`, then `diff sw.diff test.diff`.
4. Remember to remove the 'a' and 'sw.diff' files before submitting: `rm a sw.diff`.

## ex08
Double check my adding `echo` first before deleting them: `find . -type f -regex '.*\(\~\|#.*#\)$' -exec echo rm {} +`

Other options (`-delete` flag works too for file deletion):
`find . -type f \( -name '*~' -o -name '#*#' \) -exec rm {} +`
`find . -type f \( -iname '*~' -o -iname '#*#' \) -exec rm {} +`

## ex09
A magic file is a file used by the `file` command to identify a file type without relying on its file extension or metadata.

`man magic` and `man file` to learn more.

Your file should contain:
41 string 42 42 file found
!:mime file/mime-type

# Resources
https://github.com/achrafelkhnissi/1337/tree/master/Piscine-2021/DAYS/Shell00