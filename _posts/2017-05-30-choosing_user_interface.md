---
layout: post
title: Choosing type of interface in a new project
---
### My previous experience
During my studies and scientific work, I have not faced the task of creating a user-friendly and functional graphic interface. Homework is usually set to create an effective algorithm. And, of course, we do them primarily based on the basic requirements for obtaining credit. We send our solutions and pass the exams, and the written code is unlikely to be used ever - so the most I have wrote for my programs is the command line interface (getting arguments and processing flags).

In scientific work research and searching a new solution for the problem also predominates under creating useful interface. So when I faced with need to choose the best interface for the task I am solving, I went through this area. We сonsidered the following types:

- Command line interfaces
	- Argparser
	- Curses
- Graphic interfaces
	- PyQT
	- Web interface

With help of my mentor I have prepared a list of pros and cons of each type of interface regarding our task.
### Command line interfaces
* Argparser
* Curses
	+ curses will be more convenient to run on a remote servers without X11
	+ it will be easier to implement
	- perhaps it will be convenient only for advanced users
	- you will need to use some graphical interface if you want to visualise the data, but probably this is not so critical
There are also alternatives for python ncurses, for example I found http://urwid.org
### Graphic interfaces
* PyQT
	+ cross-platform
	+ easy to use
	- need to install pyqt package
	- may be slow over remote connections
* Web interface
	+ more cross-platform as you can use it even with the tablet
	+ no need to install extra packages
	+ I could add interactive charts like the one I’ve implemented in Highcharts(I could use another, open-source, library and create a graph with events’ relationships, for example https://d3js.org)
	- it can be more difficult to implement, but there are many frameworks, for example I've tried the examples from Flask http://flask.pocoo.org
	- a running web application must be accessed some way, typically over ssh forwarding, which is some hassle