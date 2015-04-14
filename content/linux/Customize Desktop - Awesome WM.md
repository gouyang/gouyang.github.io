+++
date = "2015-04-14T20:38:58+08:00"
draft = true
title = "Customize Desktop - Awesome WM"

+++

Once I have tried Awesome window manager, I will not leave it.

Awesome becomes my favor WM because it's really lightweight, and a few shortcuts meet my all needs.

I intend to make it as lean as possible with less configurations.

# First, the layouts.

There are totally 12 layouts can be used, after try each of them, I only use 3 of them now.
Maybe others is useful for some cases, which I do not aware of them becore I really know how to use them.

The three I used ared:

- floating
- tile
- max

The most used layouts by me is max, because I need a big screen for everything. Tile is used for
compare something or copy-read something, like copy content from browser to vim, some websites do not support copy.

So I comment others and use the three like this:

```
-- {{{ Tags
-- Define a tag table which hold all screen tags.
tags = {}
for s = 1, screen.count() do
    -- Each screen has its own tag table.
    tags[s] = awful.tag({ 1, 2, 3 }, s, {layouts[3], layouts[2], layouts[1]})
end
-- }}}
```

<!--more-->

# Tags

There are 9 tags by default, I do not need that much.
I only use first three tags as above codes shows.

Tags can be switched by the modkey + num. There is no need to use icon or text for them.
Actually I removed the left_layout.

```
    -- Now bring it all together (with the tasklist in the middle)
    local layout = wibox.layout.align.horizontal()
    --layout:set_left(left_layout)
    layout:set_middle(mytasklist[s])
    layout:set_right(right_layout)
```

Which just gets a more clean screen to me.

# Widget

The only widget I add is textclock.

```
mytextclock = awful.widget.textclock()

```

# shortcuts

Shortcuts is useful, I use it for the most and must used applications, like IRC(Pidgin), 
Mail Client(thunderbird), Browser(firefox, chrome), Terminal, etc.

It's okay to just have a few for most used apps, and run others from command line, it
somehow helps you to investigate other tools by manual.

For convenience, I use modkey + c to cancel/kill a window.

# Theme

Place theme in the same place for rc.lue.

```
beautiful.init(awful.util.getdir("config") .. "/themes/default/theme.lua")

```

After tested some pictures from internet, I switch over to the default background picture, which
looks awesome and awesome and awesome.

# Misc

I once have the run_once function to spawn program once, And never use it after some time.

Also, I have rules to put some app to specified tag, but not used anymore, it should be 
useful for multiscreens.

# Auto-login

There are three popular display manager: gdm, lightdm, slim.
All of them are easy to configure for autologin.

For gdm, select awesome on the login screen and make below changes:

```
/etc/gdm/custom.conf

# Enable automatic login for user
[daemon]
AutomaticLogin=username
AutomaticLoginEnable=True
```

That's it.

# conclusion

Awesome WM is a great tile window manager, it can be customized in many ways, you will find 
which suit best for you. Once you finalize your rc.lue, put it into your dotFiles on github or
somewhere else you can retrieve easily.
