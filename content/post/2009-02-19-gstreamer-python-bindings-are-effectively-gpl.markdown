---
author: juliank
comments: true
date: 2009-02-19 18:20:47+00:00
link: https://juliank.wordpress.com/2009/02/19/gstreamer-python-bindings-are-effectively-gpl/
slug: gstreamer-python-bindings-are-effectively-gpl
title: GStreamer Python bindings are effectively GPL
wordpress_id: 192
categories:
- Debian
- General
---

While most of the bindings are LGPL licensed, modules like pygst are licensed under the terms of the GPL-2+. This means, together with the fact that you need to use pygst for any application wishing to use these binding, that you can not create proprietary or non-GPL-compatible programs using the GStreamer Python bindings.

You can read more about this in the Debian Bug Tracker in [Bug#516190](http://bugs.debian.org/516190). I expect that this should be forwarded to upstream but I haven't checked their bug tracker yet. 
