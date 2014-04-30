---
layout: blog
title: Dynamic DNS, ddclient and ZoneEdit
tags: geekery
---

Like any respectable geek I have a number of domain names, this one for example, and a few others I maintain for friends and family.

For many years I've used [ZoneEdit](http://www.zoneedit.com/) for DNS for all these domains and in general it's been a reliable service. As well as normal static A and PRT records, they offer a dynamic DNS service that I've kept updated using [ddclient](http://sourceforge.net/projects/ddclient/)

Recently however I've been unable to get ddclient to work. I'm using the same configuration that I've been using for years but something's changed somewhere and now it just silently refuses to update. It's open source Perl code so I could always go fishing about in its guts to find out what's going wrong, but I have an easier solution.

In [their FAQ](http://www.zoneedit.com/faq.html), ZoneEdit suggest a simple incantation to update dynamic DNS using wget.

One quick Bash script:

    #!/bin/bash

    username='service-username'
    password='service-password'
    names='name1.example.com,name2.example.com'
    logfile='zoneedit.log'

    /bin/date > $logfile
    /usr/bin/wget --quiet -O - --http-user=$username --http-passwd=$password 'https://dynamic.zoneedit.com/auth/dynamic.html?host='$names >> $logfile```

and a crontab entry and I have a working dynamic DNS, a log file that shows me the date and result of the last update and one less root privileged demon process running on my server.