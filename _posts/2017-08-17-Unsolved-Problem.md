---
layout: post
title: 一个未解决的问题
categories: [blog ]
tags: [AngularJS, ]
description:  看以后能不能找到解决办法
---

今天做项目的时候，发现angularjs的变量在页面输出不了，变量是有值的，但就是在页面显示不出来，我一开始也是觉得可能变量没写在控制器里面，但看了源码确实在控制器里面。后来又觉得是不是html里面变量的单词写错了，仔仔细细对了好几遍也没发现错误，纠结n久，忍不住向前辈求助，前辈过来看了下，在浏览器调试了几下终于发现，原来那几个ag变量所在的div跑出了控制器的那个div，我之后想了很久也没发现为什么会跑出来，有五个div，跑出来四个，，，也没有用到浮动，不知道为什么~~

调布局没能成功，我就想着节点加载完成的时候就把那几个div appendTo到父div的后面，结果发现ag变量还是显示不出来。

最后，我机智地在父div外面又套了一个div，把控制器加到了上面，于是那几个跑出来的div里面的ag变量能成功显示了~~~

最后也没能搞明白为什么后面那几个div会跑出来，还是自己经验不足，继续努力吧！