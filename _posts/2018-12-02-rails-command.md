---
title: Rails 命令
layout: post
tags: rails
---

* **启动本地 Web 开发服务器**

```
$ rails server
```

* **创建项目**

```
$ rails new <file>
```

* **创建modal**

```
$ rails generate scaffold <modal> name:string email:string

$  rails generate model User name:string email:string
```

* **创建controler**

```
$  generate controller Users new
```

* **创建登录页**

```
$ rails generate controller Sessions new
```

* **数据迁移命令**

```
$  rails generate migration add_password_digest_to_users password_digest:string
```

* **创建resources controller**

```
$ rails g scaffold_controller User
```