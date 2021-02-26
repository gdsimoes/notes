# Some bash notes

## Shel history size

We need to add the following lines to the configuration file to increase the shell history size. `HISTSIZE` is the history size in memory and `HISTFILESIZE` is the size on file.

```shell
HISTSIZE=5000
HISTFILESIZE=10000
```

## Process Substitution

If you want to use the output of a command as a file you can use <(...) as in:

```shell
diff <(cut -d ' ' -f 5- sys.log | head) file.txt
```

## Find

You can use the command `find` to search for files. Self-explanatory example:

```shell
find / -name "*.service"
```

## Systemd

Start service:

```shell
sudo systemctl start apache2
```

Stop service:

```shell
sudo systemctl stop apache2
```

Checking the status of a service:

```shell
systemctl status apache2
```

Show current units:

```shell
systemctl
```

## nmap

Find all open ports:

```shell
nmap -p- localhost
```

## ip

To find actual ip address use:

```shell
ip a
```

A good resource to understand this output is [How-To Geek](https://www.howtogeek.com/657911/how-to-use-the-ip-command-on-linux/).

## Send public key

To send a public key to a server use:

```shell
ssh-copy-id -i keyName.pub user@serverAddress
```

## Forbid ssh from using passwords

Change `PasswordAuthentication` directive in `/etc/ssh/sshd_config` to 'no' and restart the ssh daemon:

```shell
sudo systemctl restart ssh
```

## Add user to the super user's group

```shell
usermod -aG sudo username
```

## Check logs in realtime

```shell
tail -f /var/log/auth.log
```

## Find IP address of a domain

```shell
host domain-name
```

## Site with a lot of `find` examples

[LinuxTechi](https://www.linuxtechi.com/25-find-command-examples-for-linux-beginners/)

## SFTP

SFTP is a simple and secure way of transferring files between machines. It uses the SSH configuration file, so connecting to another computer is a breeze. A lot of its commands are similar to bash, but a few are different and worth mentioning.

### Execute commands in local shell

```shell
!command
```

You can also just use `!` to go back to the local shell.

### Download file

```
get filename
```

### Download directory

```
get -r directory
```

### Upload files and directories

Same syntax as `get` but using `put` instead.

## Repeat last command

To repeat the last comand just enter `!!`. It is particularly useful when you need to repeat a command with root privileges: `sudo !!`.
