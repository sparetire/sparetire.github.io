---
layout:     post
title:      "error while loading shared libraries: libudev.so.0 解决"
date:       2015-05-18 18:42:00
author:     "Sparetire"
header-img: "img/night-sky.jpg"
---

刚在 Ubuntu 64 下下好 Cmd Markdown 客户端，运行出现错误

	lusir@FUCKGFW:~/Downloads/cmd_markdown_linux64$ error while loading shared libraries: libudev.so.0: cannot open shared object file: No such file or directory.

看起来似乎没找到 libudev.so.0 这个动态链接库，查了下做个软连接搞定

	sudo ln -s /lib/x86_64-linux-gnu/libudev.so.1 /lib/x86_64-linux-gnu/libudev.so.0

顺手记下
