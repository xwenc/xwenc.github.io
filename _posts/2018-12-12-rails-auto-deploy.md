---
title: Rails 自动化部署
layout: post
tags: rails
---

* **参考资料**
[https://ruby-china.org/topics/36899](https://ruby-china.org/topics/36899)

* **免费服务器**

[https://www.heroku.com/](https://www.heroku.com/)

* **heroku**

```
brew install heroku/brew/heroku

heroku create

heroku git:remote -a thawing-inlet-61413

git push heroku master
```