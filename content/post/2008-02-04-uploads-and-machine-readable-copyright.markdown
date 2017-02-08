---
author: juliank
comments: true
date: 2008-02-04 22:33:51+00:00
link: https://juliank.wordpress.com/2008/02/04/uploads-and-machine-readable-copyright/
slug: uploads-and-machine-readable-copyright
title: uploads and machine-readable copyright
wordpress_id: 12
categories:
- Debian
- Ubuntu
---

Two days ago, zobel uploaded some of my package updates for me.

One of them was ndisgtk 0.8.1, which adds more translations and fixes some problems. I intent to create a 0.9 release soon, with support for PolicyKit. I will upload the release candidate of this version to Debian experimental and Ubuntu Hardy.

The other upload was readahead-list 1:1.20060421.1016-1,  which I found on the Gentoo mirrors, but not where previous releases were located. This is OK, because the upstream author is a Gentoo developer and uploaded this tarball himself. I already requested to sync this release into Ubuntu Hardy, to reduce the diff between both distributions.

In both uploads, I changed the format of debian/copyright to match [http://wiki.debian.org/Proposals/CopyrightFormat](http://wiki.debian.org/Proposals/CopyrightFormat). I will also change my other packages in their next uploads, and hope that other maintainers also use the new format, especially for NEW packages.  I some cases (especially when you are upstream + packager), this format is also shorter.
