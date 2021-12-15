---
layout: post
title: "Installing Ruby 2.7"
date: 2021-12-15 23:53:00 +0900
comments: true
categories: development
tags: [assignment]
---


How to do it?

First we need a version manager like nvm (node version manager)
for ruby is rvm (Ruby version manager)

```bash
gpg --keyserver hkp://pool.sks-keyservers.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3 7D2BAF1CF37B13E2069D6956105BD0E739499BDB
```
First type this in to the terminal
and after installing the GPG keys
```bash
\curl -sSL https://get.rvm.io | bash -s stable --ruby
```
use this to install RVM stable version with ruby

but this method will install the 3.x.x version of ruby (for me it was)
so now we will going to install the 2.7.5 version to match with github pages

First we need to make sure for rvm to work properly
```bash
  echo 'source ~/.rvm/scripts/rvm' >> ~/.bashrc
```
do this for single installer in ~/.rvm/
for multi-user installed in /usr/local/rvm
```bash
  echo 'source /usr/local/rvm/scripts/rvm' >> ~/.bashrc
```

After that we will now install the ruby 2.7.5
```bash
rvm install 2.7.5
```
After the installation finished we will change the global ruby version
```bash
rvm use ruby 2.7.5 --default
```
After this, now we have installed ruby 2.7.5 on ubuntu (it works on wsl enviroment)

