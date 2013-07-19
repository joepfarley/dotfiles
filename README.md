# About my dotfiles

My .dotfiles **ViM, DWM, zsh** and I use **ArchLinux** as my linux distribution
Mainly inspired by [ornicar](https://github.com/ornicar/dotfiles). For all my programs and shell I use [solarized
colors](http://ethanschoonover.com/solarized). There are some other scripts for convenience, like
unread gmail checks, dzen2 status bar shell script and maybe other scripts which might not be needed for others at all.

## Requirements

- You will need latest **ViM** with a support of **ruby** interpreter
- **git**
- **zsh**

## Screen

![Screenshot](https://raw.github.com/l3pp4rd/dotfiles/master/screen.png)

## Installation

Clone the repository:

    clone git://github.com/l3pp4rd/dotfiles.git ~/.dotfiles

### ViM

If you do not have latest **ViM** with ruby support and all patches. You can use a shell script to install it.
**Note:** you will need GCC and all that build stuff to compile it.

    ./.dotfiles/compile/vim/build.sh

#### Terminal client

If you want nice colors with **vim** you must have a terminal client, which supports **256** colors. You may try:

- **st** does not require weird patches, does not support transparency though. You can just grab my version of
[st](https://github.com/l3pp4rd/st)
- **rxvt-unicode** you would need to compile it yourself with an option for 256 colors, may add some xft support as well.
it takes time to configure urxvt, I would suggest **st**

#### Tmux

You should consider reading about **tmux** and install it. **Tmuxinator** might come in handy after.
If you use **st** tmux will provide tabs and history scrolling support. Mouse scroll in urxvt really suck.

### Zsh

If you do not use **zsh** ignore the .zshrc installation, otherwise you could try to use it instead
of bash - install **zsh** first and use it as your default shell by running:

    chsh -s $(which zsh)

### Install modules and configurations

    cd ~/.dotfiles && git submodule update --init

Execute the setup script:

    ./.dotfiles/setup.sh

**NOTE:** most configurations use **Inconsolata** fonts, you should install or change it.

### Command-T

After that, for [command-t](http://github.com/wincent/Command-T) bundle you will need
to compile a **C** extension.

    cd ~/.vim/bundle/command-t/ruby/command-t
    ruby extconf.rb
    make

## Window Manager

If you are tired of bloated desktops like gnome, kde.. whatever, would recommend to try [dwm](http://dwm.suckless.org/)

**NOTE:** if you dwm, look how to manage it as an xsession in order to provide a possibility to be used inline
with a login manager like **slim**. You can find an examples in my dotfiles as well.

