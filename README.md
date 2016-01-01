# Ruby interface to apt-pkg

Goal of this project is to have a proper Ruby binding to APT like in
[Python](https://apt.alioth.debian.org/python-apt-doc/library/apt_pkg.html).

Currently install, remove packages commands are **not** implemented.

## INSTALL

``` console
apt install build-essential ruby-dev libapt-pkg-dev (>= 1.0)
gem install apt-pkg
```

## USING

Simple search is implemented with:

``` ruby
require 'debian/apt_pkg'
Debian::AptPkg.init
Debian::AptPkg::PkgCache.pkg_names("vim")
```

[Documentation](https://spk.github.io/ruby-apt-pkg/)

## BUILD

``` console
gem install bundler
bundle install
bundle exec rake compile
```

## TEST

``` console
bundle exec rake test
```

## LICENSE

The MIT License

Copyright (c) 2014-2016 Laurent Arnoud <laurent@spkdev.net>

---
[![Build](https://img.shields.io/travis-ci/spk/ruby-apt-pkg.svg)](https://travis-ci.org/spk/ruby-apt-pkg)
[![Version](https://img.shields.io/gem/v/apt-pkg.svg)](https://rubygems.org/gems/apt-pkg)
[![License](https://img.shields.io/badge/license-MIT-blue.svg)](http://opensource.org/licenses/MIT "MIT")
[![IRC Network](https://img.shields.io/badge/irc-oftc-blue.svg)](https://webchat.oftc.net/ "#ruby-apt-pkg")
