---
title: How to get started with Vim
category: vim
---

Hey future vimmers, Hope you are doing great. Here, I am going to share my experience about working with [Vim(the text editor)](http://www.vim.org/). Before getting started, here is some background. 

I am a front end web developer using Vim full-time for more than 4 months and believe me, since then I never had the need to open another text editor or IDE. FYI, I used to use Jetbrains Webstorm earlier. I am pretty sure this is a solid enough point for you to get motivated to invest your time learning Vim. Ok, now lets start.

I think the best way to learn vim (without quitting in the middle) is to get to a basic productive level with vim in the very beginning. Most of the devs eventually quit vim because they fail to be productive in vim during their initial learning period. So please give it a weekend to get productive before using it full-time otherwise you will most probably quit.

In this particular post, I will make you familiar with the basics needed to get work done in vim. Mind it, this one is for beginners. If you are not a beginner, please skip this post. But later, I am going to cover more advanced topics. So stay tuned for that.

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

But for completeness, I am going to cover some of the most important stuff also present in the vimtutor. Ok, let's continue now.

### Normal mode
As mentioned earlier, this is the default mode. Vim opens up in this mode. Here, every key is a command.

### Insert mode
This is the mode in which you actually write something to file(buffer actually).

### Command mode
You can enter this mode after pressing `:`(colon) in the Normal mode. This mode is used for operations like writing(saving) the file, quiting vim etc.

As I mentioned earlier, you will spend most of the time in Normal mode. So lets get familiar with some basics regarding
Normal mode.

## Movement
{% asset_img hjkl.png Plain The movement keys %}

The very basic about normal mode is how you move through text. The image above shows the left,down,up,bottom movement keys for the normal mode. You can also use the regular arrow keys(but they might not function correctly in some cases), because you need to be productive working inside vim from the very beginning.

To keep you interested, I will give you some awesomeness vim offers at regular intervals. Like for some quick movement in a file, you can use `gg` for jumping to the beginning of the file and `G` to jump to the end of file.

For jumping to a particular line number use `:<line_number>`

Jumping to next word can be achieved using `w` and similarly `b` to jump to previous word.

To quit vim,
* without taking any other action - `:q`
* without saving the current file(buffer) - `:q!`
* after saving the current file(buffer) - `:wq`

Note: you need to press Enter(Carriage) after any command in command mode(basically any command that prepends with a `:`(colon)

# Undo
To undo any change you made, press `u` in normal mode. 

# Redo
To redo any change you made, press `Ctrl + r` in normal mode. 

