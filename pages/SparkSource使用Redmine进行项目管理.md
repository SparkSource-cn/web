---
layout: page
title: SparkSource Project
description: SparkSource Project management
---

开展项目是不容易的，每个项目经理都会讲出各种项目坑和深坑——满纸荒唐言，一把辛
酸泪。

要做好项目，项目管理工具也是必要的。好的项目管理工具不但帮助团队把控进度、管理风
险，还会帮助研发跟进问题、汇总图标，让项目管理的日常工作自动化、轻松化。

SparkSource 团队使用的项目管理工具是著名的自由软件 Redmine。

Redmine 好用，但是安装比较繁琐，尤其是在 Windows 系统上安装就比较困难。大多数人
都需要安装好几次才能成功。

我们就把我们的安装经验告诉大家。

安装前提：
操作系统——Windows server 2016 DataCenter (64 bit, 2GB RAM)
数据库——MySQL 8.0
Ruby——rubyinstaller-devkit-2.6.6-1-x64.exe（虽然有2.7.1.1，但是有兼容问题。）
Redmine——redmine-4.1.1.zip (GPL v2)（直接解压就可以了。）

准备数据库：
以 MySQL 管理员身份登录到 MySQL，并执行

```
CREATE DATABASE redmine CHARACTER SET utf8mb4;
CREATE USER 'redmine'@'localhost' IDENTIFIED BY 'password';
GRANT ALL PRIVILEGES ON redmine.* TO 'redmine'@'localhost';
```

目的是为 Redmine 创建数据库及其用户，当然它们的名字和密码可以根据情况自己改。注
意这里要修改一下，数据库用户的认证插件以便兼容。

```
USE mysql;
SELECT USER,PLUGIN FROM USER WHERE USER='redmine';
ALTER USER 'redmine'@'localhost' IDENTIFIED BY 'password' PASSWORD EXPIRE NEVER;
ALTER USER 'redmine'@'localhost' IDENTIFIED WITH mysql_native_password BY 'password';
FLUSH PRIVILEGES;
```

连接数据库：
复制已经解压的 Redmine 目录下的 config/database.yml.example 文件为
config/database.yml，并做修改

```
  production:
  adapter: mysql2
  database: redmine
  host: localhost
  username: redmine
  password: "password"
```

安装 Redmine 依赖：
这个步骤容易有错误，不过都可以根据提示解决。打开终端，进入
Redmine 根目录，并执行

```
gem install bundler
bundle config set without 'development test rmagick'
gem install thin
```

然后就可以生成 Redmine 使用的数据

```
bundle exec rake generate_secret_token
set RAILS_ENV=production
set REDMINE_LANG=zh
bundle exec rake db:migrate
bundle exec rake redmine:load_default_data
```

如果期间报告 enventmachine 相关的错误，重新安装可以解决

```
gem uninstall eventmachine
gem install eventmachine --platform=ruby
```

启动 Redmine 服务：
以上安装结束，可以启动服务看看，

```
ruby bin/rails server thin -e production -p 3001
```

然后到浏览器打开

```
http://localhost:3001
```

你应该看到 Redmine 的欢迎页面。可以使用默认账号登录

>账号：admin

>密码：admin

登录后就可以按照手册配置项目了。其中，邮件配置根据邮件服务商的不同略有差异，不过
主流邮件服务商都有模板支持，包括 QQ 邮箱、163 邮箱以及 Gmail 等。

千里之行，始于足下。创建好项目，开始工作吧。

请同时参看：
 - [SparkSource 优雅处理高端仪表应用界面](Project/SparkSource_优雅处理高端仪表应用界面.html)
