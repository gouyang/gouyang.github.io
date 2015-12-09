+++
date = "2015-09-06T20:24:21+08:00"
draft = true
title = "ssh always ask password even public key is uploaded"

+++

ssh with public key works for a really long time, but it just goes wrong these two days.
At first I was just tried to delete old publick key files, re-generate it and upload them, but it seems not enough. 

<!--more-->

The problem is that the user home dir ownership and file mode changed on remote host, although I have no idea how it changed. Maybe get hacked?
To debug the problem, look at /var/log/secure may get some clues.


