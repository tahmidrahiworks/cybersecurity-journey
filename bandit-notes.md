1. Password found in level 0 < 1: 6y2kwnwK6grgvwvpvLaa2T1cpFEKOhNR

2. Password found in level 1 < 2: PK8fYLZg2hnHSz83plBL1iEPKdD3QToB

    Lesson: Where we find any filename with a character like -, we use ./ before that file to treat this as a normal file.

3. Password found in level 2 < 3: 7ZZ2LFrykP2zEyvBl4m3clcL7tGYJPME

    Lesson: Here to see what's inside a file whose filename has spaces in it and to treat this as a file, we need to add ./....... to see what is inside.

4. Password found in level 3 < 4: xzTXq1rDJQVVAzdv5cHq1TQytTWufAMq

    Lesson: Here the file was hidden inside a directory, and to see this hidden file we have to use the command ls -a inside that directory to display the hidden file.
 
5. Password found in level 4 < 5: 6C7h9GD8M6ai5nr7wo1RonrzFjj9yIrG

    Lesson: Here we have to find human-readable text among some files inside a directory. Using the command file ./* we can find the file containing ASCII text information that is in a human-readable language.

6. Password found in level 5 < 6: pXa26xhMWaC2SvDotA4r9EgZkulOeSBW

    Lesson: First we have to use the command find . -size 1033c ! -executable to find the file containing the password. We use this command so that it matches the given properties.

7. Password found in level 6 < 7: Bmnnvf82KzQlfxgAI2d1zYbr1u9pr3E3

    Lesson: To find that, we have to use the command find / -user bandit7 -group bandit6 -size 33c 2>/dev/null to find it.

8. Password found in level 7 < 8: VR1ljMayciFxbnUokuQmJFw6QC9VKtub

    Lesson: Here we found this using a smart command that is grep "millionth" data.txt.

9. Password found in level 8 < 9: EjmOSvuAu7sGAHqHVcBDPirRe9T03kxl

    Lesson: Here we use the command sort data.txt | uniq -u. sort lists all the matching lines together and uniq -u filters out everything that repeats, leaving us with just one password line.

10. Password found in level 9 < 10: B0s2khmbT9u0geKuOoVGW3JZKhndE3BG

    Lesson: Here we used the command strings data.txt or we can use strings data.txt | grep "=" to find the exact line we wanted.
Password found in level 10 < 11: pYfOY6HwUsDj5rL9UvyhU7MCmv8vN5Ro

    Lesson: Here we used the command base64 -d data.txt to decode the password (and we can turn readable data into base64 form by using the command echo "text" | base64 and to save the transformed language in a separate file we use the command echo "text" | base64 > "file").

11. Password found in level 11 < 12: GROozWPO8QyN0mGrjUkID0WCYkZiQxrN

    Lesson: The command we used was cat data.txt | tr 'A-Za-z' 'N-ZA-Mn-za-m'. This command helps us translate Caesar cipher or ROT13 texts to readable text.

12. Password found in level 12 < 13: qQYQiHOBPR8zR61qxYqX45quvihF2uzk

    Lesson: Here we have to do a cycle of decompression and extraction to get the result with the help of tar for extraction and bzip2 and gzip for decompression.

13. Password found in level 13 < 14:

    Lesson: Here we actually don't get the password; we use the passkey found in a file to log into lab 14 < 15.

14. Password found in level 14 < 15: pbLYuZtTg4MgaqfJx8jbA9gKKGqM68A7

    Lesson: Here we get this password using Netcat when we used the command nc localhost 30000 using the password found in bandit14 which is bandit14's password using the command (cat /etc/bandit_pass/bandit14).
eee
15. Password found in level 15 < 16: kS0Hf0u5HiXFwKMKFqXvPdOTNGGa0X8V

    Lesson: Here we get this password using the command openssl s_client -connect localhost:30001 by giving it the level 15 password that is pbLYuZtTg4MgaqfJx8jbA9gKKGqM68A7.

16. password found in Level 16 < 17:

    Lesson: Password was not found in level 16 < 17 for login on bandit17. Instead, we found a passkey to login on bandit17 using the commands (nmap -sV -p ports localhost) and (openssl s_client -connect localhost:port_number -quiet).

17. Password found in level 17 < 18: OQxXZjELndr90zuhOTDYBEomI0SZITXI

    Lesson: Here we found this using the command diff passwords.new passwords.old.

18. Password found in level 18 < 19: KpsOfPkcP7i1FlIExk2QEjyt6dw8dxZI

    Lesson: Here we found it by using another technique because on level 18 the target user's login script (such as .bashrc or .profile) was explicitly configured to run the exit command or print "byebye". Here we used the command ssh bandit18@bandit.labs.overthewire.org -p 2220 "cat readme" to get what we wanted without keeping a shell open.

19. Password found in level 19 < 20: 4pIjcunZ0fK2vmp3IwfG8Vf7VhxD6pOA

    Lesson: Here we got this by running a program we found using command—first = ./bandit20-do, but we got the password using this command = ./bandit20-do cat /etc/bandit_pass/bandit20.

20. Password we found in level 20 < 21: bW9kBv5WC3P4yoDyf12LSdGuNz5ka6hY

    Lesson: Here we found this by opening a server first by the command nc -lvnp 1234 and then in another terminal when we ran ./suconnect it waits for the current level password. When it is fed with the password, it shows the next level password (and we can also try with another command that is echo "current level password" | nc -lvnp 1234 to get the password directly when executed).

21. Password found in level 21 < 22: RYVux2rHEm9tiXHmLFzuR7Vhx6AZQMEz

    Lesson: Here we found this by using the command cat /etc/cron.d/cronjob_bandit22 first to see what script is running, and then we use the command cat /usr/bin/cronjob_bandit22.sh to find where the script is processing its data, and after that we used the command cat /tmp/t7O6lds9S0RqQh9aMcz6ShpAoZKF7fgv to see the password.

22. Password found in level 22 < 23: gKXDTAXnIz3OBxiPjRZ2uqutUlPZrBsw

    Lesson: Here we did the same thing we did in level 21 < 22, but with some modification because here the script uses a dynamic, randomized filename inside the /tmp folder generated using an MD5 hash of the username (I am user bandit23). Here we manually simulated what the script does by hashing the string using the command echo I am user bandit23 | md5sum | cut -d ' ' -f 1 by following the path we found in the script.

23. Password we found in level 23 < 24: hVQMk3lJNsmQ7VF3ubyrNNBom7BOgVXv

    Lesson: Here we did perform a real privilege escalation attack by using our script that is:
    Bash

    #!/bin/bash
    cat /etc/bandit_pass/bandit24 > /tmp/password.txt
    chmod 666 /tmp/password.txt

    First we made this script in nano and then copied this script into the folder by using this command "cp /tmp/myscript.sh /var/spool/bandit24/foo/". After that we have to wait 1 or 2 minutes and then we can see the password.

24. Password found in level 24 < 25: SoHfqMOEqIX2IYKVciZxvgpR9a2Djx4P

    Lesson: Here we found this by using a brute-force method. First we made a temporary folder and then in that folder we made a script:
    Bash

    #!/bin/bash
    for i in {0..9}{0..9}{0..9}{0..9}
    do
        echo "hVQMk3lJNsmQ7VF3ubyrNNBom7BOgVXv $i" >> list.txt
    done

    And then we saved this file, and after executing this we got our list file named list.txt. Then we see inside the list file using command cat list.txt, and then we pipe the list.txt information into netcat using command "cat list.txt | nc localhost 30002" and then we got the password.

25. The password we found in level 25 < 26: jHdv2ELQhT22BkprMNDjybZDAkw1zeBJ

    Lesson: Here we found this using a method named shell escape exploit. For this, first we have to see inside /usr/bin/showtext to see what happens when we try to login using the private key of level 26 we found from the previous level. Then we login using that private key for level 26 by making the terminal small enough to see the more option. When we saw that more option, we typed v to open the vi editor, and then we used command ":set shell=/bin/bash". This tells vi "when I ask for a shell, use /bin/bash". Then we used command ":shell", which tells the shell to launch that shell now. After that we eventually logged into bandit26 and we saw the password for bandit26 using command "cat /etc/bandit_pass/bandit26".

    The core concept: The server forced me into more instead of bash. more was programmed to close the session when it finished. I made the terminal tiny so it would pause. Then I pressed v to enter vi, and from vi I launched a new bash shell. I didn't delete more, I just escaped it and got a real shell instead.

26. The password we found in level 26 < 27: STJLJBRRphMxKB392CT4iOr5CbzPU9ER

    Lesson: Here we found this using privilege escalation. First we ran command cat /etc/bandit_pass/bandit27 and it said permission denied because it was the file owned by bandit27. But we found another file named bandit27-do which is an executable file with SUID enabled. So when we ran it, it ran as bandit27. After that we used command ./bandit27-do cat /etc/bandit_pass/bandit27 and this helped us to get the password for the next level because we ran that SUID-enabled program.

27. Password we found in level 27 < 28: y8Yd2ssKcpHpud7UvOSOxwamRMzIGIeQ

    Lesson: Here we found this with a very important concept in cybersecurity. At first we cloned the repository from bandit27 which was git enabled, which helped us to clone the file. We used the command "git clone ssh://bandit27-git@bandit.labs.overthewire.org:2220/home/bandit27-git/repo" to clone the repo to my account. It got copied into my account and we found the copied folder, and there we found the file inside it called README, where we got the password of the next level that is 28.

28. Password we found in level 28 < 29: Em7eGtqaMySwNFjCpwzzHhLhospOcdt0

    Lesson: Here we found this using the same method we used in level 27 < 28, but here the password was hidden. To find this password, we have to use the command "git log" first to see the list of commits, and then we used the command "git show <commit hash from the log>" and after typing that command we eventually got the password.

29. Password we found in level 29 < 30: jq9Dfg2rXsfYsWMgFuKlXhphjdH7USgX

    Lesson: Here we also found a git repository which we copied to our home using command "git clone ssh://bandit29-git@bandit.labs.overthewire.org:2220/home/bandit29-git/repo". Then we tried to read the file, but we couldn't because the password was hidden. So we tried to see the password by going through its branches using command "git branch -a", and there we found a location called remotes/origin/dev where developers usually forget to erase the data. Then by using the command "git checkout remotes/origin/dev", we teleported from the public master universe into the secret dev universe. Then when we see what's inside the README.md file, we can find the password. It means we were looking at a saved snapshot of a branch, but we weren't actively editing it.

30. Password we found in level 30 < 31: 82NkymblpGBYmIXG6ZQ8YldBYstHpfUf

    Lesson: Here we found this by also cloning the repository from level 30, and then we couldn't find the password because it was hidden. So we used another trick where the developers use tags to mark versions. A tag in git is like a sticky note attached to a specific point in the project's history. Here we used the command "git tag" first, which showed us a sticky note named secret. When we used the command "git show secret" to see what's inside that note, we saw our password for level 31.

31. Password we found in level 31 < 32: pWuj5jBQ6IgV0NXwiH6g1pXRF8S1YvbT

    Lesson: Here we found this by following the instructions we saw inside the README.md file. First we used command = echo "May I come in?" > key.txt. Then we used command = git add key.txt to put this in the staging area (waiting room), but because the developers put key.txt in the .gitignore file, it denied us. So we forced it using command = git add -f key.txt. Then we used command = git commit -m "Forced key.txt" because now the file was in the waiting room, but it's still not saved permanently in history. git commit takes all the files in the waiting room, packs them into a neat little box, and we used -m here to seal it with a message. Then we used command = git push origin master to take the sealed box from my computer and physically upload it to the OverTheWire server. When the server received the box, it opened it, ran its script, saw the text "May I come in?", and handed us the password for the next level.

32. Password found in level 32 < 33: u4P2CyPOwPGLe94RdD9Uo2FxFwvnFswM

    Lesson: Here after logging in, we couldn't see or use our normal shell because the developers made a custom shell here which replaces our normal commands with uppercase letters, and that's why we can't use our commands. That's why we used command = $0 so that the system launches a new normal shell for us. But we also didn't get our environment to work fully because it's a new shell and it doesn't know where to find basic commands like PATH. To fix that, we used command = export PATH=/usr/bin:/bin. Then we used command cat /etc/bandit_pass/bandit33 to get the password for the next level.

