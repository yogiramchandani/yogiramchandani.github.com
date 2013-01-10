---
layout: post
title: Persisting aliases in cmd
tags:
- cmd
- dos
---

***doskey*** - The DOS equivalent of the Linux command ***alias*** doesn`t persist when cmd.exe launches again.

The quickest fix is to script this to run during the initialisation of cmd.exe.

1. Create the script aliases_initialise.cmd in your directory_of_choice (i.e. c:\directory_of_choice\aliases_initialise.cmd) and enter your aliases

{% highlight cmd %}
@echo off
cls
doskey clear=cls
doskey ls=dir
{% endhighlight %}

2. Run the command

{% highlight cmd %}
reg add "hkcu\software\microsoft\command processor" /v Autorun /t reg_sz /d c:\directory_of_choice\aliases_initialise.cmd
{% endhighlight %}

Bang! you're done.
