+++
date = "2010-02-22 17:04:38"
title = "a custom epiphany location bar"
draft = "false"
categories = ["technical"]
tags = ["epiphany", "gnome", "gtkrc", "monospace", "pgo"]
author = "jamesjustjames"
+++

since i do much research on the internets, i often find myself in a web browser. my favourite of the lot is <a href="http://projects.gnome.org/epiphany/">epiphany</a>. this post isn't about its merits or failures, but about the awesome way to make my location bar be exactly how i like it: monospaced.

just add the following into your ~/.gtkrc-2.0 file and then restart epiphany. feel free to modify as you wish.

```
# ~/.gtkrc-2.0
style "Epiphany_Locationbar" {
# leave out the font size if you wish
font_name = "Monospace 12"
#bg[NORMAL] = "#ff0000"
}</code>

<code> </code>

<code># both of these seem to work...
#widget "*.EphyLocationEntry.*" style "Epiphany_Locationbar"
widget_class "*.EphyLocationEntry.*" style "Epiphany_Locationbar"
```
thanks to <a href="http://raphael.slinckx.net/blog/2006-03-01/epiphany-url-entry-in-monospace">raphael</a> for the original post, and the #epiphany developers.
