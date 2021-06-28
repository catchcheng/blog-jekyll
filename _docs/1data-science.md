---
title: Data Science
tags:
  - jekyll
  - github
description: Projects including NLP, ML, and CV Areas.
---

# Data Science

## Speech and Language Processing

Coming soon!

## Machine Learning with Python

Coming soon!

## Personal Blogs Website

As you can see here, it is my personal static website using Jekyll template. After downloading ruby and Jekyll, you can choose a template you'd love to edit, and then make your own website and deploy it on Github server to make it live.

Building your own website makes it much easier to do the customizations with your own design, style, and interests. All you need is a bit of coding, including HTML, CSS, JS. Looks hard at the first sight, but it totally worths learning and practising it if you really care to present on your own design.

### Here is how to install the prerequisites software

Initially (on OS X), you will need to setup [Brew](http://brew.sh/) which is a package manager for OS X and [Git](https://git-scm.com/). To install Brew and Git, run the following commands:

```bash
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
brew install git
```

If you are on Debian/Ubuntu, then you can easily install git with `apt-get`

```bash
apt-get update && apt-get install -y git
```

#### Install Jekyll

You can also install Jekyll with brew.

```bash
$ brew install ruby
$ gem install jekyll
$ gem install bundler
$ bundle install
```

On Ubuntu I do a different method:

```bash
git clone https://github.com/rbenv/ruby-build.git ~/.rbenv/plugins/ruby-build
echo 'export PATH="$HOME/.rbenv/plugins/ruby-build/bin:$PATH"' >> ~/.bashrc
exec $SHELL
rbenv install 2.3.1
rbenv global 2.3.1
gem install bundler
rbenv rehash
ruby -v

# Rails
curl -sL https://deb.nodesource.com/setup_4.x | sudo -E bash -
sudo apt-get install -y nodejs
gem install rails -v 4.2.6
rbenv rehash

# Jekyll
gem install jekyll
gem install github-pages
gem install jekyll-sass-converter

rbenv rehash
```
