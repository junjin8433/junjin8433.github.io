---
layout: post
section-type: post
title: Install ruby2.0+ on mint/ubuntu
category: tech
tags: [ 'skills' ]
---

### Install ruby2.0+ on mint/ubuntu
since the default version of ruby on ubuntu&mint is **1.9**, we need to install **2.0+** version by hand

```zsh
sudo apt-get install python-software-properties
sudo apt-add-repository ppa:brightbox/ruby-ng
sudo apt-get update
sudo apt-get install ruby2.1 ruby2.1-dev
```

### Use the mirror of taobao
While doing bundle install, it may ouccur some unexpaced errors, to solve this,we use the mirrors of **taobao.org** to fix.

```zsh
gem sources --remove https://rubygems.org/
gem sources -a https://ruby.taobao.org/
gem install rails
bundle config mirror.https://rubygems.org https://ruby.taobao.org
bundle install
```
