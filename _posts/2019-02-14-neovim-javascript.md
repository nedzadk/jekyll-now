---
layout: post
title: Setting up [Neo]Vim for easier project navigation
---

## Intro

I've been struggleing for some time to switch my JS development to Vim, but always ended up with struggle of navigating through JS projects quick enough. 

I have tried all kind of plugin combination but never felt quite comfortable. 

But than I discovered [`Universal ctags`](https://github.com/universal-ctags/ctags) and vim plugin [`vim-gutentags`](https://github.com/ludovicchabant/vim-gutentags), and Vim felt like home. 

## Installation

### Universal ctags

You need to clone repository, compile and install universal ctags. No reason to worry it is very simple process, here is what i had to do on my system (i am running Ubuntu 18.04.1):

```bash
$ cd
$ git clone https://github.com/universal-ctags/ctags
$ cd ctags
$ ./autogen.sh
$ ./configure
$ make
$ sudo make install
```

### vim-gutentags

Depending on your plugin manager you need to add following in your neovim init script or .vimrc:

```
Plug 'ludovicchabant/vim-gutentags'
```

If you are not sure where your Vim/NeoVim configuration is located you can, start [n]vim and type following:
```
:e $MYVIMRC
```
This will open your [n]vim configuration file ready for editing.


Once you are done with all this restart [n]vim and run in case you are using `VimPlug` following:
```
:PlugInstall
```

After installation is completed, restart [n]vim and that's it, you have setup ctags to work on all your projects. Tags file will be generated automatically each time you open project. 



