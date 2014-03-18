---
title: Lua - An Introduction
author: rob
date: 2013-03-18
template: article.jade
---

***
##Note: This is the first part in a multi-part series on using Lua in a variety of situations. 

Parts of this article series:

> - [Lua - An Introduction](#) (this article)
> - [Lua - Basic Embedding with C++](#) (Planned - Under development)
> - [Lua - Basic Embedding with .NET](#) (Planned - Under development)

***
###What is Lua?

Lua is a scripting language with an official implementation (pure ANSI C) which can be embedded and used across many platforms.
It was created over 2 decades ago and has grown to become what is arguably one of the most popular scripting languages aside from the monster that is Javascript.

Lua is everywhere. Many software products such as Redis, Apache HTTP Server and Wireshark use it to allow for other developers to quickly extend their functionality.
If you have ever played World of Warcraft or League of Legends, you have used a product that leverages the speed and flexibility of Lua.

It was designed with extensible semantics in mind. This allows for developers to create a [domain specific language](http://en.wikipedia.org/wiki/Domain-specific_language) particular to their project.
This means that if a developer desires to add classes and object-oriented functionality, he could simply implement it using some of Lua's features <a href="http://en.wikipedia.org/wiki/Lua_(programming_language)#Object-oriented_programming">Example - Wikipedia</a>.

###Some command line examples

To demonstrate the basic features of the Lua interpreter, we will download it and try out some commands.
You can grab the latest official source from [lua.org](http://www.lua.org/ftp/). Building this is trivial on almost every platform since it is written in ANSI C.

For Unix users (This example on Ubuntu Server 12.04 LTS):
```
mkdir lua
cd lua
wget http://www.lua.org/ftp/lua-5.2.3.tar.gz
tar -xvzf lua-*
cd lua-5.2.3
make ansi
cd src
```

For windows users the commands and process vary depending on your C++ development tools and environment.
To follow along easily you can get a pre-built installation package with some tools from [here](https://code.google.com/p/luaforwindows/downloads/list).

You can now run commands once you launch the interpreter.

**Printing 'Hello World'**
```
ubuntu@ubuntu:~/lua/lua-5.2.3/src$ ./lua
Lua 5.2.3  Copyright (C) 1994-2013 Lua.org, PUC-Rio
> print('Hello World');
Hello World
```

##More examples here soon.



