# Some bash notes

## Shel history size

We need to add the following lines to the configuration file to increase the shell history size. `HISTSIZE` is the history size in memory and `HISTFILESIZE` is the size on file.

```
HISTSIZE=5000
HISTFILESIZE=10000
```

## Process Substitution

If you want to use the output of a command as a file you can use <(...) as in:

```
diff <(cut -d ' ' -f 5- sys.log | head) file.txt
```

## Find

You can use the command `find` to search for files. Self-explanatory example:

```
find / -name "*.service"
```

## Systemd

Start service:

```
sudo systemctl start apache2
```

Stop service:

```
sudo systemctl stop apache2
```

Checking the status of a service:

```
systemctl status apache2
```

Show current units:

```
systemctl
```
