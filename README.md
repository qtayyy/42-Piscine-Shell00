# 42-Piscine-Shell00

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
6. `touch -t 202406012047 test0; touch -t 202406012146 test1; touch -t 202406012245 test2; touch -t 202406012344 test3; touch -t 202406012343 test4; touch -t 202406012344 test5; touch -h -d "2024-06-05 22:20:00" test6`
7. `chmod 714 test1; chmod 504 test2; chmod 404 test3; chmod 641 test4; chmod 404 test5; chmod 777 test6; chmod 715 test0`

## ex03
id_rsa_pub is the public key file generated when you create an SSH key pair using tools like ssh-keygen
1. `ssh-keygen`
2. Press <Enter> three times
3. cd ~/.ssh
4. cat id_rsa_pub
