- Arithmetics: User double parenthesis to enable arithmetics operations. Example: count=(($count+2))
- While loop syntax: while [ condition ] do ... done
- If statement syntax: if [ condition ] ; then ... else ... fi
- Writing commands that can be fed into prompts: here commands. 
    - Example: ftp -n 1.2.3.4<<myCmdFeed
    -          quote USER joe
    -          quote PASS 1234
    -          ls
    -          myCmdFeed //marks end of here command
- bash command substitution: you can use the result of a command as input in bash scripts by using the following syntax: < <(command) (http://unix.stackexchange.com/questions/52026/bash-how-to-read-one-line-at-a-time-from-output-of-a-command)
- Reading line by line: you can use the following format: 
    while read line; do
        xxxx (use "$line" to access the current line)
    done