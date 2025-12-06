# shellme

`shellme` plays scripted commands (type and execute) in a interactive shell as it is done by a human.

Can be used to create simple demos to record with other tools, so you don't have to really type commands in good timing and without mistakes to record a demo video.

`shellme` just spawn an interactive shell using `expect` and is expecting shell prompt, then it type first command and press enter (execution) then wait to get next prompt...

(no commands with interactive response can be used, shellme only launch commands on prompt, use directly `expect` if you need interactivity)

```
# shellme "echo This is a demo" "ls -l"
```

## usage

```
shellme -f <commands_file>
shellme <cmd>...
```
