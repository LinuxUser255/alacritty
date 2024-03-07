<p align="center">
    <img width="200" alt="Alacritty Logo" src="https://raw.githubusercontent.com/alacritty/alacritty/master/extra/logo/compat/alacritty-term%2Bscanlines.png">
</p>
<h1 align="center">Alacritty:  Blazingly Fast terminal emulator!</h1>

![Alacritty_my_README](https://github.com/LinuxUser255/alacritty/assets/46334926/f4ac6aa7-312a-4b9a-a41a-74bda7bfe70d)






## About

Alacritty is a modern terminal emulator that comes with sensible defaults, but
allows for extensive [configuration](#configuration). By integrating with other
applications, rather than reimplementing their functionality, it manages to
provide a flexible set of [features](./docs/features.md) with high performance.
The supported platforms currently consist of BSD, Linux, macOS and Windows.


The software is considered to be at a **beta** level of readiness; there are
a few missing features and bugs to be fixed, but it is already used by many as
a daily driver.

Precompiled binaries are available from the [GitHub releases page](https://github.com/alacritty/alacritty/releases).

## About this fork
This one is aimed at Linux and supporting use for legacy versions.
</br>
Also, 
### This repo includes a config file! 
### In fact, it includes two of them!
</br>

The configuration file for Alacritty is named `alacritty.toml`, and is located in the config directory of this repo.
</br>
This fork is licensed under thr [GPL3](https://www.gnu.org/licenses/gpl-3.0.en.html)

## Features

You can find an overview over the features available in Alacritty [here](./docs/features.md).

## Installation

Alacritty can be installed by some Linux distro's package managers.
It may be in Debian 12's apt.
Regardless, you can use this fork to build from source
And can do so easily using the included install script.
See instructions below.


### Debian, and Debian-based distributions:

### 1. Run the installation script
```sh
curl -LO https://raw.githubusercontent.com/LinuxUser255/alacritty/master/scripts/alacritty_install.sh
sh alacritty_install.sh
```

### 2. Setting up the configuration file `alacritty.toml`

The `alacritty.toml` goes in `~/.config/alacritty`.
You will have to make the alacritty directory yourself.

After you have made the `.config/alacritty` directory, then `curl -LO` which ever config you want listed below, and move it to `~/.config/alacritty`
Remember, do this from your home directory.

</br>

Making the alacritty directory in your `.config` directory
```sh
mkdir .config/alacritty
```
</br>

Move the `alacritty.toml` to the `.config/alacritty` directory
```bash
mv alacritty.toml -t  ~/.config/alacritty
```
</br>

This is a generic `alacritty.toml`
```sh
curl -LO https://raw.githubusercontent.com/LinuxUser255/alacritty/master/config/alacritty.toml
```
</br>

This is a custom config:
```sh
curl -LO https://raw.githubusercontent.com/LinuxUser255/alacritty/master/alacritty_config/alacritty.toml
```
</br>

More istall and build instructions to install Alacritty can be found
[here](INSTALL.md).

### Requirements

- At least OpenGL ES 2.0

## Configuration

You can find the documentation for Alacritty's configuration in `man 5
alacritty`, or by looking at [the website] if you do not have the manpages
installed.

[the website]: https://alacritty.org/config-alacritty.html

Alacritty doesn't create the config file for you, therefore, **_The maintainer of this fork included it for you!_**
</br>

That convenience, nor the convenience of an auto install script is not included in the original alacritty repo.
</br>

The configuration file is sourced/read from following locations:
The default is ` ~/.config/alacritty`

1. `$XDG_CONFIG_HOME/alacritty/alacritty.toml`
2. `$XDG_CONFIG_HOME/alacritty.toml`
3. `$HOME/.config/alacritty/alacritty.toml`
4. `$HOME/.alacritty.toml`

**_Why isn't feature X implemented?_**

Alacritty has many great features, but not every feature from every other
terminal. This could be for a number of reasons, but sometimes it's just not a
good fit for Alacritty. This means you won't find things like tabs or splits
(which are best left to a window manager or [terminal multiplexer][tmux]) nor
niceties like a GUI config editor.

[tmux]: https://github.com/tmux/tmux
