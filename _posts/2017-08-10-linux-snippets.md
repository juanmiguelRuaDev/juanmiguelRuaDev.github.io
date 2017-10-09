---
layout: post
title:  "Linux snippets"
image: ''
date:   2017-08-10 00:06:31
tags:
- linux
- shell
- snippets
description: 'Linux snippets'
categories:
- Snippets
serie: learn
---


## Linux snippets

Throughout my life as professional I ever had bad memory. In fact, I signed up in every new on-line platform such like _Evernote_, _google keep_, _remember the milk_, etc. hoping to be able to remember every interesting post/snippet that help me in the future.

For this reason, I decided to collect all those linux scripts that you knows that exist but never remember how exactly is spelled out.


### SO information

In this section, there are a serie of useful scripts that might give you information about your linux distribution. Information such as the SO version, hard drive space, etc.

#### LIN-01: Linux distribution information
```bash

lsb_release -a

```


#### LIN-02: Find process with `ps` and `grep`
```
ps aux | grep <process_name>
```

#### LIN-02: Zip and unzip files
```
unzip <filename> -d <dir>
```
