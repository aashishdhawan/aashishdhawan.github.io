---
layout: post
title:  "Open pull request from Terminal"
date:   2016-03-30 00:00:00
author: aashish
categories: Technical iOS
---

Whenever i am done with my awesome feature in my feature branch, i go to github and create pull request manually. This changed today. Now i have a script which makes it super easy.

Save the following script in `/usr/local/bin/` with a name `git-open-pr` and give it permissions to make it executable by `chmod +x get-open-pr`

<script src="https://gist.github.com/aashishdhawan/7e264da4fc176a7157bc49af548154b8.js"></script>

When you are done with your feature, Push it and type `git open-pr` and see the magic yourself.

You can find the gif [here](http://aashishdhawan.github.io/images/Demo_gif_open_pr.gif)
