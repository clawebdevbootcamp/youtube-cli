# youtube-cli
### A minimal command to play media from youtube

## Introduction
This is the concluding project of Unit 3 of the web development bootcamp offered by [Code Labs Academy](https://codelabsacademy.com), in this unit we had an introduction to backend development in javascript, we touched on many of the theory concepts in networking that makes communication over the internet possible. We learned about NodeJs as a server side framework, we leveraged the variety of built-in modules that it offers and we saw how to serve static and dynamic files from the server using templating engines. We will use all these concepts and more throughout our journey with Nodejs, but first let’s discover another way of using node js: as a scripting and automation tool. We will be building our own command-line interface (CLI) called “youtube-cli”. Finally we will install “youtube-cli” to make it easy for us to use from anywhere locally.

But first and foremost, we will introduce command-line interfaces (CLIs) and then explore the packages needed for building this project and the steps to follow to reproduce it.

## Understanding CLIs
A command line interface or a CLI is a command line or terminal program that accepts text input to execute a task and optionally produces an output. A great example of this sort of commands we could write is **git**.

All CLI programs come with a help message to guide users when utilizing this tool, and a typical help for a command is as follows:
```
$ date --help
 Displays or sets the date.

DATE [/T | date]

Type DATE without parameters to display the current date setting and
a prompt for a new one. Press ENTER to keep the same date.

If Command Extensions are enabled the DATE command supports
the /T switch which tells the command to just output the
current date, without prompting for a new date.
```
During this project, we will be creating a fully functional (help messages included) CLI program called “youtube-cli” that we will be able to run directly from the terminal in linux or the command line in windows.

## Project Description
We mentioned the name of the project a lot to this point, but we haven’t discussed the functionalities offered by the program we will be building, and from the name of it, we can guess that it is something in relation to youtube.

We will be building a tool that searches for a youtube video and then plays it, in audio or video format, using the **vlc** player. The process of doing so is simple, we will be using **third-party packages** to help us execute tasks quickly (like searching for youtube videos and getting video information), and we will proceed as follows:

1. Expect a query as input to our program.
2. Use a package to search for that query in youtube and get a list of search results
3. Use a simple selection method to select the correct video to play from that list (for example always select the first video).
4. Get the streaming url of the video (this url is different than the simple youtube link, and is needed in order to play a video outside of the youtube website)
5. Run VLC media player and pass it the url and it will be loaded successfully!

Seems easy, right! 
Don’t worry, a step by step guide will be shown next to help you while creating this tool. Let’s start with the input (aka options and arguments)

The most basic version of our tool with have the following options and commands:
- Global **choice** option:  choose the item you want to play manually instead of relying on the default selection method.
- Global **limit** option: the limit of search items to get from youtube. We can set the default number to 10 for example.

- **Audio** command: only launches the audio for the selected video.
- **Video** command: launches the audio and video for the selected video.
  - **Quality** option: used to select the quality of the video to launch (this is functionality is ***optional***)
 
> Note that these are options and arguments needed for our project, but you can be as creative as you want and add more functionalities. 

> ## Hints and guidance
> Trying to do this project on your own will help you develop yourself in a huge way as you will learn many new concepts and discover helpful packages.
> 
> But to make this experience a bit easier on beginners just starting NodeJS, and make it less time consuming, we included a milestone with a list of issues that will walk you through the process of building this project and give you hints and pieces of code to make your life easier.

Feel free to do this project on your own, or take a glance at the provided hints.

HAPPY CODING YALL :D
