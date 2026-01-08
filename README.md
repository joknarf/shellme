[![Joknarf Tools](https://img.shields.io/badge/Joknarf%20Tools-Visit-darkgreen?logo=github)](https://joknarf.github.io/joknarf-tools)
[![Build and Release Packages](https://github.com/joknarf/shellme/actions/workflows/release.yml/badge.svg)](https://github.com/joknarf/shellme/actions/workflows/release.yml)
[![Shell](https://img.shields.io/badge/shell-bash%20|%20zsh%20|%20ksh%20-blue.svg)]()
[![Licence](https://img.shields.io/badge/licence-MIT-blue.svg)](https://shields.io/)
[![Packages](https://img.shields.io/badge/Packages-%20rpm%20|%20deb%20|%20pkg%20|%20apk%20|%20brew%20-darkgreen.svg)](https://github.com/joknarf/shellme/releases/latest)

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
