# 南京大学 IT 侠

系统 [Jekyll](jekyllrb.com/docs/quickstart/)
主题 [forty](https://github.com/andrewbanchich/forty-jekyll-theme)

*建议使用 Git 远程更新，不要直接在网站上更改*

## 本地测试

*要求安装 ruby 与 ruby-gem *

``` sh
git clone https://github.com/NJU-itxia/home.git
cd home
gem install bundler #太慢记得换源
bundle install
bundle exec jekyll server #本地运行
bundle exec jekyll #查看其他命令
```
如果要在docker运行，需按照以上配置镜像，为减少麻烦可以用：
```
docker run [各种参数] [镜像名] bundle exec jekyll server -H 0.0.0.0
```
做好端口映射后便可外部访问

## 目录结构

``` sh
.
├── _config.yml # 配置文件
├── assets
│   ├── css
│   ├── fonts
│   ├── images # 图片存放位置
│   └── js
│
├── index.md # 主页
├── introduction.md # 介绍页面
├── donation.md # 捐赠页面
├── recruiment.md # 招新页面
├── service.md # 服务页面
├── document.md # 共享文档
├── coroperation.md # 合作页面（未发布）
├── board_games.md # 桌游目录页面
│
├── _data # 数据存储
│   ├── budget_list.yml # 资金去向公示
│   ├── donation_list.yml # 捐赠列表 
│   ├── index_url.yml # 首页模块
│   ├── president.yml # 鼓楼主席
│   └── president_xianlin.yml # 仙林主席
│
├── _includes
│   ├── footer.html # 底部导航栏文件（联系我们、友情链接等）
│   ├── head.html
│   ├── header.html # 导航栏
│   └── tiles.html
│
├── LICENSE.md
├── README.md
├── favicon.ico 
├── ...
│
└── _site # 静态文件存放位置
                                                                   
```

## 使用

### 增加页面或者更新

- 新建 `page.md`
- 增加头文件
```
---
title: YOUR-TITLE
layout: post
image: 
--- 
```
- 在头文件后增添内容
- 如需将链接加入首页模块，请编辑 `./_data/index_url.yml`
- 注意`./_config.yml`内的`tiles-count`一项数字对应于主页的模块数，需要同步修改。

### 更新介绍与捐赠页面

介绍页面涉及到主席团的更替，捐赠页面也需要实时更新。

具体请直接参考`./_data`下的 .yml 文件。

> 格式很简单，请务必注意缩进

