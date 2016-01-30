---
title: How to get started with Vim
category: vim
---

Hey future vimmers, Hope you are doing great. Here, I am going to share my experience about working with [Vim(the text editor)](http://www.vim.org/). Before getting started, here is some background. 

I am a front end web developer using Vim full-time for more than 5 months and believe me, since then I never had the need to open another text editor or IDE. FYI, I used to use Jetbrains Webstorm earlier. I am pretty sure this is a solid enough point for you to get motivated to invest your time learning Vim. Ok, now lets start. P.S. I am writing this also on Vim :D .

I think the best way to learn vim (without quitting in the middle) is to get to a basic productive level with vim in the very beginning. Most of the devs eventually quit vim because they fail to be productive in vim during their initial learning period. So please give it a weekend to get productive before using it full-time otherwise you will most probably quit.

In this and the next few posts, I will make you familiar with the basics needed to get work done in vim. Mind it, this one is for absolute beginners. If you are not a beginner, please skip this post. But later, I am going to cover more advanced topics. So stay tuned for that.

## What is a buffer?
In vim, when you open a file, that file is opened in the memory in a buffer. The changes you made are written to buffer, not to the file until you write the buffer to file using `:w` , `:update` etc. So, do not get confused when I use the term "buffer". It essentially means file (although it isn't file actually).

## Installation
First of all, install vim (I am not going to explain this, you can easily get the instructions online). Open a terminal and open vim.
```
$ vim
```

You should see something like this:
{% asset_img initial-screen.png Plain Vim's Initial Screen %}

Cool. Now this is the NORMAL mode. It's called the normal mode because this is the mode you will spend most of your time in. In this mode, almost every key on the keyboard is a command. So be careful with your fingers. Now there are many modes. But to start with, you need to know only three modes:
* Normal
* Insert
* Command
  

Now before continuing, I will strongly recommend you to go through vimtutor. It's the built in tutorial(actually it's just a text file) in vim that will explain you many of the basics needed to get started with vim. To open vimtutor, open a terminal and type
```
$ vimtutor
```

But for completeness, I am going to cover some of the most important stuff here(also present in the vimtutor). Ok, let's continue now.

### Normal mode
As mentioned earlier, this is the default mode. Vim opens up in this mode. Here, every key is a command.

### Insert mode
This is the mode in which you actually write something to file(buffer actually).

### Command mode
You can enter this mode after pressing `:`(colon) in the Normal mode. This mode is used for operations like writing(saving) the file, quitting vim etc.

As I mentioned earlier, you will spend most of the time in Normal mode. So lets get familiar with some basics regarding Normal mode.

## Movement
{% asset_img hjkl.png Plain The movement keys %}

* The very basic about normal mode is how you move through text. The image above shows the left,down,up,bottom movement keys for the normal mode. You can also use the regular arrow keys(but they might not function correctly in some cases), because you need to be productive working inside vim from the very beginning.

* You can use `gg` for jumping to the beginning of the file and `G` to jump to the end of file.

* For jumping to a particular line number use `:<line_number>`

* Jumping to next word can be achieved using `w` and similarly `b` to jump to previous word.

## To quit vim,
* without taking any other action - `:q`
* without saving the current file(buffer) - `:q!`
* after saving the current file(buffer) - `:wq`

Note: you need to press Enter(Carriage) after any command in command mode(basically any command that prepends with a `:`(colon)

## Search
Pressing `/` in normal mode followed by a string will search the string in the current line. 

## Replace
To replace something, use `:%s/patterntobereplaced/resultingpattern/g`. This will replace the occurrence of 'patterntobereplaced' be 'resultingpattern'. You can replace the last portion in the above command with `/gc` to ask for confirmation before replacing.

## Editing
### Undo
To undo any change you made, press `u` in normal mode. 

### Redo
To redo any change you made, press `Ctrl + r` in normal mode. 

### Delete a line
To delete a line, press `dd`. To delete a line and start typing, press `cc`.

# Seed .vimrc file
You can use this vimrc config to get you some useful settings for vim. https://gist.github.com/AvinashKrSharma/cd3f7a15989081e8ab16

To use it, you need to copy it into the home folder in Linux. For windows and mac, please check online about where to keep the vimrc file. After placing the file at the right location, just open vim and Vundle will install. Vundle is one of the many plugin managers for vim. I prefer Vundle because using Vundle, all you need for managing your plugins in vim is a single vimrc file, and Vundle does the rest for you.

Let's take a look at what's included in the vimrc.

The first portion of the file installs Vundle if it's not already present. Next comes the various settings to enable useful features in vim.

* `syntax enable`: enables syntax highlighting

* `set autoindent`: enables automatic indentation of lines when you move to new line

* `set backspace`: specifies what <backspace>, CTRL-W, etc. can do in Insert mode

* `set colorcolumn`: shows a vertical line after 80 characters in the buffer, acting as a guide line to prevent you from writing long lines in your codes.

* `set cursorline`: highlights the currentline you are at.

* `set gdefault`: enables operations to occur globally on the buffer, like search, replace etc.

* `set hlsearch`: highlights the matching patterns when you search for something.

* `set ignorecase`: enable case-insensitive operations by default.

* `set incsearch`: start searching on every key you press while searching for something.

* `set nolist`: hides invisible characters like EOL etc.

* `set noswapfile`: disable swap file. You don't need it at this moment.

* `set nobackup`: disable backup file.

* `set laststatus=2`: always show the status line at the bottom, to always show the colorful status line.

* `set number`: show line number.

* `set showmatch`: when inserting a bracket, briefly jump to its match.

* `set smartcase`: if you type a capital letter in the search pattern, the search becomes case sensitive.

* `set mouse=a`: enable mouse. Try it :D

* The next three lines are for showing available commands when you are in command mode and hit tab while typing a command.

* `let mapleader="\<Space>"`: sets a leader key. Leader key is a user set key that can be used to create custom key mappings for various vim commands and actions.

### Plugins

The following two lines are required by Vundle:
`set rtp+=~/.vim/bundle/vundle/`  
`call vundle#begin()`

### Now the plugins
* **Nerdtree**: Well, we all are habitual of that handy project explorer. Nerdtree gives us that project explorer. To use it, you need to enter the command `:NERDTree`.

* **Syntastic**: Probably the best syntax highlighting(or atleast the most famous one) plugin for vim(P.S. I use Neomake now). 

* **CtrlP**: The fuzzy file finder. To use it, you need to press <Ctrl+P>(the default key mapping).

* **Airline**: The very useful and beautiful status line at the bottom.

* **TComment**: To comment any line in you code with just a key binding(Ctrl+\_ Ctrl+\_).

### Mappings
I created 3 mappings here.

* `<Space>c`: To comment a line.

* `<Space>i`: To indent whole line. `gg` takes us to the top of the file, `=` indents the lines upto `G` i.e. the last line effectively indenting the whole file.

* `<Space>n`: To toggle the project explorer tree.

I am going to explain mappings in detail in the upcoming post. For now just use them. Although if you are curious, you can always look up and learn more about them.

## Summary
I hope you will feel better using vim now. Mind it, this is a very beginner level post so that no beginner feels overwhelmed on the first day and still finds vim easier to use to some extent. I strongly recommend you to go through vimtutor earlier mentioned in this post. That covers the basics very well.

In the next post I will mention some more important settings and plugins, how to make custom key maps, and much more. Stay tuned.
