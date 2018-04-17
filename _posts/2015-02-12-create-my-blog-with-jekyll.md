---
layout: post
title:  "《精力管理》"
date:   2015-02-15 22:14:54
categories: reading notes
tags: reading notes
---

* content
{:toc}



## 第一部分 如何做到全情投入

### 第一章 什么事精力及如何管理精力

##说在前面##

* 精力就是做事情的能力。包括体能、情感、思维、意志四个方面。
* 我们所有的想法、情感和行为都对精力有积极或消极的影响。
* 精力，而非时间， 是高效表现的基础
* 你一定要全情投入，优秀表现的难度在于，它需要从各个方面更有效地管理精力，达到最终目标。
* 高效表现源于有技巧的精力管理。 
* 领导者正是团体精力的统筹人。他们首先要具备个人精力管理技巧，然后才能调动、集中、投入和维持团队的集体精力。 
* 全情投入是确保最优表现的最佳精力状态。

##精力管理的四个基本原则##

* 原则一： 全情投入需要调动四种独立且相关联的精力源： 体能，情感，思维和意志
* 原则二： 因为使用过度和使用不足都会削弱精力， 必须不时更新精力以平衡消耗。
* 原则三： 为了提高能力，我们必须突破自己的惯常极限， 模仿运动员进行系统训练。
* 原则四： 积极的精力仪式习惯，即细致具体的精力管理方法， 是全情投入、保持高效表现的诀窍。“仪式习惯”指的是定义明确、具有高度计划性的行为。

## 管理精力的三个步骤 ##

* 明确目标
* 面对现实。制定变革的计划离不开对个人现状的清醒认知。
* 付诸行动。 用实际行动缩小“现实的我”与“理想的我”

### 第二章 成功人士罗杰遇到的5个障碍

* 体能不足是罪魁祸首
* 情感账户告急
* 徒劳地强打精神
* 到底什么最重要

### 用RubyGems安装Jekyll

### 创建博客

## 后续

*  整个安装过程参考了jekyll官网，注意jekyll还有一个简体中文官网，不过比较坑（我就被坑了），有些内容没有翻译过来，有可能会走弯路，建议如果想看中文的相关资料，也要中英对照着阅读。[jekyll中文网 http://jekyllcn.com](http://jekyllcn.com), [jekyll英文网 http://jekyllrb.com](http://jekyllrb.com)
*  jekyll中的css是用sass写的，当然直接在`_sass/_layout.scss`中添加css也是可以的。
*  本文是用Markdown格式来写的，相关语法可参考： [Markdown 语法说明 (简体中文版) http://wowubuntu.com/markdown/](http://wowubuntu.com/markdown/)  
*  按照本文的说明搭建完博客后，用`github Pages`托管就可以看到了。注意，在github上面好像不支持rouge，所以要push到github上时，我将配置文件_config.yml中的代码高亮改变为`highlighter: pygments`就可以了
*  博客默认是没有评论系统的，本文的评论系统使用了多说，详细安装办法可访问[多说官网 http://duoshuo.com/](http://duoshuo.com/)，当然也可以使用[搜狐畅言 http://changyan.sohu.com/](http://changyan.sohu.com/)作为评论系统。
*  也可以绑定自己的域名，如果没有域名，可以在[godaddy http://www.godaddy.com/](http://www.godaddy.com/)上将域名放入购物车等待降价，买之。
*  祝各位新年快乐！

---

## 可能出现的问题

### `hitimes/hitimes (LoadError)`

**错误代码：**

```
C:/Ruby22/lib/ruby/2.2.0/rubygems/core_ext/kernel_require.rb:54:in `require': cannot load such file -- hitimes/hitimes (LoadError)
```

**解决方法：**

在stackoverflow上又一个很好的解决方法。[hitimes require error when running jekyll serve on windows 8.1](http://stackoverflow.com/questions/28985481/hitimes-require-error-when-running-jekyll-serve-on-windows-8-1) 虽然上面的题主问的是 win 8.1 系统下的情况，但是同样适用于 win7。下面我简单翻译一下错误原因和解决方法。

> 可能是 Ruby 2.2 和 hitimes-1.2.2-x86-mingw32 中有一些 ABI 变化，少了一些相关的类库。
>
> 所以卸载 hitimes 并通过 `--platform ruby` 重装即可。代码如下：

```
gem uni hitimes
**Remove ALL versions**
gem ins hitimes -v 1.2.1 --platform ruby
```

> 然后将自动重新编译 hitimes 并适用于 Ruby 2.2

下面是我自己的卸载和安装过程：

```
E:\GitWorkSpace\gaohaoyang.github.io>gem uni hitimes

You have requested to uninstall the gem:
        hitimes-1.2.2-x86-mingw32

timers-4.0.1 depends on hitimes (>= 0)
If you remove this gem, these dependencies will not be met.
Continue with Uninstall? [yN]  y
Successfully uninstalled hitimes-1.2.2-x86-mingw32

E:\GitWorkSpace\gaohaoyang.github.io>gem ins hitimes -v 1.2.1 --platform ruby
Fetching: hitimes-1.2.1.gem (100%)
Temporarily enhancing PATH to include DevKit...
Building native extensions.  This could take a while...
Successfully installed hitimes-1.2.1
Parsing documentation for hitimes-1.2.1
Installing ri documentation for hitimes-1.2.1
Done installing documentation for hitimes after 1 seconds
1 gem installed
```


关于，[hitimes](https://rubygems.org/gems/hitimes/versions/1.2.2) 是一个快速的高效的定时器解决方案库，详情可以去官网查看。
