

## constructing command inside of editor

If we need to execute long command line or need to run multiple command line all at once we can use use text editor.


```bash
ctrl + x + e
```

This will open up text editor, we can create long command and multiple line for each command, save and exit. 

```bash
ctrl + o
ctrl + x
```

## creating super fast writing area with ram

If we need area which can write and read super fast we can take some resouces from RAM and mount as diskspace here.

```bash
mdkir -p /mnt/ram

mount -t tmpfs tmpfs /mnt/ram -o size=1024M
```

## editing last command inside of text editor

Fix the last command we run inside of text editor if we made any mistake with this command.

```bash
fc
```

This will open up text editor with the last command we run inside of this and we can edit the command from here.


## creating tunnel with ssh command

We can use network from network ssh with our local environment. The network will went thru the ssh machine and pass to the local machine.

The command format is local_port:hostname:remote_port for example:

```bash
ssh -L 3337:127.0.0.1:6379 root@192.168.1.100 -N
```

Meaning the traffic for the local network on the port 3337 will pass thru the remote machine host root@192.168.1.100:6379

Then we use the port using this commmand:

```bash
redis-cli -p 3337
```
## creating subsequent folder name

We can creating variation of folder and subfolder under the subfolder using one simple command.

```bash
mkdir {sub1, sub2}/{sub1, sub2, sub3}
```

The command will create folder path sub1/sub1, sub1/sub2, sub1/sub3, sub2/sub1, sub2/sub2, sub3/sub3.

## exit terminal without terminating process

The command is the combination of disown command and exit terminal command. We disown any running process and exit the terminal leaving the running process continue executing.


```bash
disown -a && exit
```



































