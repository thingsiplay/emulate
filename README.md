# emulate

RetroArch run script and playlist extractor

- **Author**: Tuncay D.
- **License**: [MIT License](LICENSE)
- **Source**: [Github source](https://github.com/thingsiplay/emulate)

## Introduction

Two little helper scripts, with the focus to run games from your RetroArch
installation in **Linux** without using the RetroArch GUI. A working
environment is required, as these scripts just work on top of RetroArch.

The script "emulate" will run a ROM file associated to its core. Manual editing
of the script is most likely required, if your setup differs from mine. The
script "playlist" on the other hand is a good companion for extracting paths
from RetroArch playlists. It can deliver a list of all paths, or just the last
played game or offer a dmenu/rofi GUI menu to select a game.

Both scripts can be combined like this:

```
playlist last | emulate
```

## Usage of script "emulate"

There are two main ways of usage: 1. registering filetypes on system level to
this script and 2. explicit commandline call

### File extension registering

To associate the file extension to the script, right mouse click on the ROM
file, select "open with..." and choose the script ("emulate"). The script will
run the associated emulator core from RetroArch. From now on, you should be
able to play the games by double clicking the files in your favorite graphical
file manager.

### Commandline

Alternatively you can also run the script from commandline without registering
file extensions at system level. When run through commandline, at least the
path to the ROM file is required, which can be relative or include "~" for HOME
as well. No wildcards are supported, make sure to resolve links to a single
file. An optional system name as the second argument can be given, which will
resolve to the core path. This can be useful for file extensions, which are not
associated to a single core, like "bin" or "chd".

It will also read from stdin, if something is there and no argument is
specified.

```
emulate ROM [SYSTEM]
emulate "Pinball Dreams (U).smc"
emulate "~/Emulator/roms/gb/Super Mario Land (W) (V1.1) [!].gb" gb
playlist last | emulate
```

## Configuration

The configuration is done through editing the script files itself.

1. Set variable `config_file` to your actual "retroarch.cfg" file.
2. Change or add new cores to the list of cores.
3. Associate file extensions to the cores.


## How it works

text

## Installation and Requirements

text

## Feedback

If you want report a bug or have any questions, then [leave me a message](https://thingsiplay.game.blog/contact/) on my contact page.
