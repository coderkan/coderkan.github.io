---
layout: post
title: "Explore the Git Log and Customize Visualizing."
description:
headline: 
modified: 2019-06-13
category: git
tags: [git, software, github, gitignore]
imagefeature: 
mathjax: 
chart: 
comments: true
featured: true
---


Hi everyone,

GUI tools make our work easier. Today, many people prefer the use of these tools. I always prefer terminal based systems instead of these interfaces. In particular, I don’t need to use any GUI in the **git** tool.

My friends often criticize my use of the terminal instead of the GUI. But I think the terminal environment is more flexible and useful.

My friends say that the GUI is a good option, especially for more comfortable observations of commitments. I will try to show you what we can do with the terminal against this situation.

I will elaborate with a few examples.

Firstly, we can check with


>git log --graph


<div align="center">
    <script id="asciicast-254357" src="https://asciinema.org/a/254357.js" async ></script>
</div>

Another usage of git log is with `--decorate` and `--oneline` command. This commands show you a logs with oneline and decorated.

>git log --graph --decorate --oneline

<div align="center">
    <script id="asciicast-254358" src="https://asciinema.org/a/254358.js" async ></script>
</div>

More customizable command is like that

>git log —graph —full-history —all —color —pretty=format:”%x1b[31m%h%x09%x1b[32m%d%x1b[0m%x20%s"

<div align="center">
    <script id="asciicast-254359" src="https://asciinema.org/a/254359.js" async ></script>
</div>


>git log — graph — pretty=format:’%Cred%h%Creset %ad %s %C(yellow)%d%Creset %C(bold blue)<%an>%Creset’ — date=short

<div align="center">
    <script id="asciicast-254360" src="https://asciinema.org/a/254360.js" async ></script>
</div>

You want to change how you want your pretty format. I will change format as below command.

>git log — graph — pretty=format:’%Cblue%h%Creset %ad %s %C(yellow)%d%Creset %C(bold red)<%an>%Creset’ — date=short

<div align="center">
    <script id="asciicast-254361" src="https://asciinema.org/a/254361.js" async ></script>
</div>


    %H →commit hash
    %h →abbreviated commit hash
    %T →tree hash
    %t →abbreviated tree hash
    %P →parent hashes
    %p →abbreviated parent hashes
    %an →author name
    %aN →author name (respecting .mailmap, see git-shortlog[1] or git-blame[1])
    %ae →author email 
    %aE →author email (respecting .mailmap, see git-shortlog[1] or git-blame[1])
    %ad →author date (format respects — date= option)
    %aD →author date, RFC2822 style
    %ar →author date, relative
    %at →author date, UNIX timestamp
    %ai →author date, ISO 8601-like format
    %aI →author date, strict ISO 8601 format
    %cn →committer name


For more information about git log, you can visit its official web page.

You can see full version of using git log, please check out [asciinema](https://asciinema.org/a/251391).

<div align="center">
    <script id="asciicast-251391" src="https://asciinema.org/a/251391.js" async ></script>
</div>

Using the terminal, I can print the screen in the format I want. In short this is ease of use for me.

I hope your thoughts about using the terminal have changed a bit.

Good works.