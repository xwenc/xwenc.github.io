---
title: 用rbenv升级ruby版面
layout: post
tags: ruby
---

安装rbenv
```
  git clone https://github.com/rbenv/rbenv.git ~/.rbenv
```
[https://gist.github.com/sandyxu/8aceec7e436a6ab9621f](https://gist.github.com/sandyxu/8aceec7e436a6ab9621f)

刷新安装列表： 

```
  brew upgrade rbenv ruby-build
	rbenv install --list
	rbenv install 2.7.0
```

切换版本:  
```
  rbenv global 2.7.0
```

安装gem
```
	gem sources
	gem sources --add https://rubygems.org/
```

升级redis
```
 brew upgrade redis
```
[https://www.36nu.com/post/74.html](https://www.36nu.com/post/74.html)

[https://ruby-china.org/wiki/install_ruby_guide/](https://ruby-china.org/wiki/install_ruby_guide/)

[https://github.com/rbenv/rbenv#uninstalling-ruby-versions](https://github.com/rbenv/rbenv#uninstalling-ruby-versions)

[https://github.com/rbenv/ruby-build](https://github.com/rbenv/ruby-build)