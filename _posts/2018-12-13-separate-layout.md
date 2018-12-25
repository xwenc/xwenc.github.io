---
title: Rails 两套layout
layout: post
tags: rails
---

admin 单独做一套 layout 可以这样来
1. controller 中建一个 admin 的文件夹
2. admin 文件夹中建一个 application_controller.rb 的文件，
   class Admin::ApplicationController < ApplicationController
     layout "admin"
   end
   其他的contoller 继承 Admin::ApplicaitonController
3. layout 文件夹中，建一个 admin.html.erb，内容参考 application.html.erb

[https://stackoverflow.com/questions/42926596/separate-frontend-assets-from-admin-assets](https://stackoverflow.com/questions/42926596/separate-frontend-assets-from-admin-assets)

[https://api.rubyonrails.org/classes/ActionView/Layouts.html](https://api.rubyonrails.org/classes/ActionView/Layouts.html)