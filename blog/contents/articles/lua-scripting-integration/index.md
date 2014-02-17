---
title: Lua Scripting Integration
author: rob
date: 2013-02-17
template: article.jade
---

This article will cover the fundamental concepts of integrating a scripting language (Lua in the case) into an application.

The core idea is that, by using a scripting language to define the behavior of an application, developers do not need to recompile the project to test the changes. Simply modify the script file(s) and run the executable again. Some applications can even be designed to reload scripts dynamically to evaluate changes at run-time.

The motivation for all of this may not be immediately obvious to developers not used to working with C++. Long story short, small code changes in a large C++ project can result in a lengthy build process which is usually constrained at certain stages (primarily linking) to a single-thread of operation. Imaging changing a single integer and needing to wait 20 minutes before testing the outcome.  One could certainly use a configuration file or database to store such information (and you should), but let us consider some other cases. 

What if we have a series of C++ class instantiations and method calls that have to be made in response to an event or condition? Consider the following semi-real world example for handling a player spell cast in a popular video game:

```c++
//Pseudo C++ code for casting a spell in League of Legends
```

If you wanted to add/remove a method call or change the triggering condition above the entire executable would need to be rebuilt.  This would be a nightmare for gameplay designers who very frequently change spell mechanics for balancing purposes or adding of new features.



