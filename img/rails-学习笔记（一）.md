---
title: rails 学习笔记（一）
date: 2016-08-18 22:32:25
tags:
---
rails学习了几天，很多内容比以前更加清晰，
- 创建用户资源rails g model user username:string password_digest:string
- 创建控制器rails g controller users new create
- 使用脚手架创建模块和框架 rails g scaffold todo
- 使用gem bcrypt加密密码
- 登录功能使用session控制器，以下为对应的路由
 - get '/login', to: 'sessions#new'           # 获取登录表由
 - post '/login', to: 'sessions#create'       # 登录路由
 -  delete '/logout', to: 'sessions#destroy'   # 登出路由
- 将user与todo关联rails g migration AddUserToTodos user:references（user_id:references 是说把 user_id 作为外键添加到 todo 表结构中）
