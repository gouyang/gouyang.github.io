+++
date = "2015-09-06T19:52:02+08:00"
draft = true
title = "Set default browser in terminal"

+++

How to set the default browser in terminal for every applications?   

I've searched this and figured it out long time before, but still spend lots of time to find the answer today.
It seems the perfectly way is, add below contents to ~/.local/share/applications/mimeapps.list.

<!--more-->

```
[Default Applications]
x-scheme-handler/http=google-chrome.desktop
x-scheme-handler/https=google-chrome.desktop
x-scheme-handler/ftp=google-chrome.desktop
x-scheme-handler/chrome=google-chrome.desktop
text/html=google-chrome.desktop
application/x-extension-htm=google-chrome.desktop
application/x-extension-html=google-chrome.desktop
application/x-extension-shtml=google-chrome.desktop
application/xhtml+xml=google-chrome.desktop
application/x-extension-xhtml=google-chrome.desktop
application/x-extension-xht=google-chrome.desktop

[Added Associations]
x-scheme-handler/http=google-chrome.desktop;
x-scheme-handler/https=google-chrome.desktop;
x-scheme-handler/ftp=google-chrome.desktop;
x-scheme-handler/chrome=google-chrome.desktop;
text/html=google-chrome.desktop;
application/x-extension-htm=google-chrome.desktop;
application/x-extension-html=google-chrome.desktop;
application/x-extension-shtml=google-chrome.desktop;
application/xhtml+xml=google-chrome.desktop;
application/x-extension-xhtml=google-chrome.desktop;
application/x-extension-xht=google-chrome.desktop;

```

Thunderbird has something special, there is a knowledge base provides a completed guide about it.
http://kb.mozillazine.org/Default_browser
