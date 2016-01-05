---
title: How to get started with Vim
category: vim
---

Hey future vimmers, Hope you are doing great. Here, I am going to share my experience about working with [Vim(the text editor)](http://www.vim.org/). Before getting started, here is some background. 

I am a front end web developer using Vim full-time for more than 4 months and believe me, since then I never had the need to open another text editor or IDE. FYI, I used to use Jetbrains Webstorm earlier. I am pretty sure this is a solid enough point for you to get motivated to invest time in Vim. Ok, now lets start.

I think the best way to learn vim (without quitting in the middle) is to get to a basic productive level in vim in the very beginning. Most of the devs eventually quit vim because they fail to be productive in vim during their initial learning period. So please give it a weekend to get productive before using it full-time otherwise you will most probably quit.

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

### Normal mode
As mentioned earlier, this is the default mode. Vim opens up in this mode. Here, every key is a command.

### Insert mode
This is the mode in which you actually write something to file(buffer actually).

### Command mode
You can enter this mode after pressing `:`(colon) in the Normal mode. This mode is used for operations like writing(saving) the file, quiting vim etc.
