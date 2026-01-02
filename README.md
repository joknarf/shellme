# shellme

`shellme` plays scripted commands (type and execute) in a interactive shell as it is done by a human.

Can be used to create simple demos to record with other tools, so you don't have to really type commands in good timing and without mistakes to record a demo video.

![shellme](https://github.com/user-attachments/assets/584957b6-89c2-4ade-b5ed-638bfdbd16d1)

`shellme` just spawn an interactive shell using `expect` and is expecting shell prompt, then it type first command and press enter (execution) then wait to get next prompt...

(no commands with interactive response can be used, shellme only launch commands on prompt, use directly `expect` if you need interactivity)

```
# shellme "echo This is a demo" "ls -l"
```

## prerequisites

* expect

## usage

```
shellme [--prompt <regexp>] [--sleep <before_s> <after_s>] \
        [--speed <base_ms> <jitter_ms>] \
        [-f <file_with_commands>] | <cmd1> <cmd2> ...

  regexp    : regexp to expect to get prompt, default '\n?.*[$#] $'
  before_s  : seconds to wait before typing, default 2
  after_s   : seconds to wait after typing, default 2
  base_ms   : typing char mseconds, default 120
  jitter_ms : typing jitter mseconds, default 120
```
