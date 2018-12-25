---
title: Rails Active Record
layout: post
tags: rails
---

* **命名约定**
Rails 把模型的类名转换成复数，然后查找对应的数据表。例如，模型类名为 Book，数据表就是 books。数据库表名：复数，下划线分隔单词（例如 book_clubs, 模型类名：单数，每个单词的首字母大写（例如 BookClub）

* **模式约定**

外键：使用 singularized_table_name_id 形式命名，例如 item_id，order_id。创建模型关联后，Active Record 会查找这个字段；
主键：默认情况下，Active Record 使用整数字段 id 作为表的主键。使用 Active Record 迁移创建数据库表时，会自动创建这个字段；

还有一些可选的字段，能为 Active Record 实例添加更多的功能：

created_at：创建记录时，自动设为当前的日期和时间；
updated_at：更新记录时，自动设为当前的日期和时间；
lock_version：在模型中添加乐观锁；
type：让模型使用单表继承；
(association_name)_type：存储多态关联的类型；
(table_name)_count：缓存所关联对象的数量。比如说，一个 Article 有多个 Comment，那么 comments_count 列存储各篇文章现有的评论数量；