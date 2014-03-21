---
layout: post
title: Persisting aliases in Windows
tags:
- cmd
- batch
- bash
---

The ***doskey*** command (cmd.exe) and ***alias*** command (bash) don't persist between sessions. bash gives us a config file we can save the commands to for persistence but cmd has no such file.
 
##Persisting doskey (cmd)

For cmd the quickest fix is to script this to run during the initialisation of cmd.exe.

1. Create the script aliases_initialise.cmd in your directory_of_choice (i.e. c:\directory_of_choice\aliases_initialise.cmd) and enter your aliases

{% highlight bat %}
@echo off
cls
doskey clear=cls
doskey ls=dir
{% endhighlight %}

2. Run the command

{% highlight bat %}
reg add "hkcu\software\microsoft\command processor" /v Autorun /t reg_sz /d c:\directory_of_choice\aliases_initialise.cmd
{% endhighlight %}

##Persisting alias (bash)

1. Create a .bashrc file under ~/.bashrc (~ is usually /c/Users/<username>)

{% highlight bash %}
$ notepad ~/.bashrc
{% endhighlight %}

2. Add your aliases to the file, save and restart the session.

{% highlight bash %}
alias ..='cd ..'
alias ...='cd ../../../'
alias .4='cd ../../../../'
alias .5='cd ../../../../..'
{% endhighlight %}

