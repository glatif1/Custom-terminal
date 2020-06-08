# Custom Terminal Shell

A customized terminal shell which can be modified to give specific information in any format. Implemented using the lowest level functionality of C by using System Calls. 

Features: 
  -	Scripting :
  
            Example Scripting File:
            
            cat <<EOM | ./crash
            ls /
            echo "hi"
            exit
            EOM

            # Which outputs (note how the prompt is not displayed):
            bin  boot  dev  etc  home  lib  lost+found  mnt  opt  proc  root  run  sbin  srv  sys  tmp  usr  var
            hi

            # Another option (assuming commands.txt contains shell commands):
            ./crash < commands.txt
            (commands are executed line by line)
            
  -	Built-In Commands
    - cd to change the CWD. 
    - '#' (comments): strings prefixed with # will be ignored by the shell
    - History prints the last 100 commands entered with their command numbers
    - ! (history execution): entering !39 will re-run command number 39, and !! re-runs the last command that was entered.
    - exit to exit the shell. (^C is ignored)
  -	Redirection:
  
        // Creates/overwrites 'sorted_pwd.txt' and redirects the output of sorted passwords file there there:
        ╭─[🙂]─[14]─[username@mymachine:~]
        ╰─╼ cat /etc/passwd | sort > sorted_pwd.txt

 To Run:
 
    $> make
    $> ./shell

To exit:

    $> exit
