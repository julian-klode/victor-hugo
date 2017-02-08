---
author: juliank
comments: true
date: 2014-04-09 12:57:59+00:00
link: https://juliank.wordpress.com/2014/04/09/thinkpad-x230-uefi-broken-by-setting-a-setting/
slug: thinkpad-x230-uefi-broken-by-setting-a-setting
title: ThinkPad X230 UEFI broken by setting a setting
wordpress_id: 670
categories:
- General
tags:
- lenovo
- thinkpad
- uefi
- x230
---

Today, I decided to set my X230 back to UEFI-only boot, after having changed that for a bios upgrade recently (to fix a resume bug). I then choose to save the settings and received several error messages telling me that the system ran out of resources (probably storage space for UEFI variables).

I rebooted my machine, and saw no logo appearing. Just something like an underscore on a text console. The system appears to boot normally otherwise, and once the i915 module is loaded (and we're switching away from UEFI's Graphical Output Protocol [GOP]) the screen works correctly.

So it seems the GOP broke.

What should I do next?
