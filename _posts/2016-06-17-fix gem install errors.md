---
layout: post
section-type: post
title: fix gem install errors
catefory: tech
tags: ['tutorial']
---

## gem install errors

if ```gem install``` causes error like

```
ERROR:  While executing gem ... (Gem::RemoteFetcher::FetchError)
    Errno::ECONNRESET: Connection reset by peer - SSL_connect (https://api.rubygems.org/quick/Marshal
    .4.8/bundler-1.12.5.gemspec.rz)
```
that must be caused by GFW(Great Firewall of China), thus we need to change the source to taobao.org.

```
gem sources --remove https://rubygems.org/
gem sources -a https://ruby.taobao.org/
gem sources -l
```
if it looks like:

```
***CURRENT SOURCES***

https://ruby.taobao.org
```
then you have only one source taobao.org


