- To start an SSH listener session on Fedora, execute command "service sshd start"
- You can use ssh-keygen to generate keys. You can specify the type with the -t option (e.g. ssh-keygen -t rsa)
- You can set up shortcuts to SSH connection by creating a config file under $(USER_HOME)/.ssh. The content should look something like this:
    Host <name of shortcut>
        Hostname <ip or domain name of host>
        Port <port to which you wish to connect>
        User <user name you will use to connect>
        IdentityFile <path to private key that pairs with the public key you registered with the host>
    For other options, see http://www.cyberciti.biz/faq/create-ssh-config-file-on-linux-unix/
- SSH Tunneling: Sometimes, you may need to gain access to a machine that is only accessible through another machine . If you have SSH access rights to the intermediate machine, you can try to establish an SSH tunnel between you and the target machine. The command is: ```ssh user@<host of intermediate machine> -L <port you want to expose>:<host of target machine>:<port exposed by target machine>.``` For example, if your machine can't access facebook, but you know 111.222.33.44 can, you can execute command ```ssh -L 9090:facebook.com:80 111.222.33.44```, then you can access facebook by visiting localhost:9090. 
- Using login bash shell to execute scripts: If a script executes properly when you ssh using an interactive shell or su - after logging in using a non-interactive shell, but doesn't work when you ssh non-interactively without su -, try executing the script with "bash -l"
- Check sshd config: sshd -T