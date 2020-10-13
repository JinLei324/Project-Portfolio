# Vue.js+Django 
# 一、后端项目（back-end-src目录）

## 1. 架构说明

1. Xadmin+Django2全家桶（①django；②django-REST-framework；③django-filter；④django-simple-captcha；⑤django-REST-framework-jwt；⑥django-favicon）

## 2. 使用教程（下面的命令皆以back-end-src为当前目录运行）

1. 环境搭建。安装好`Python3.5`或者`Python3.6`后，命令行运行`pip install -r python-lib-requirements.txt`（注意，请保证你使用的Django版本要至少为2.0）
2. 数据库生成。修改`APP_Inventor_case_base/settings.py`中的DATABASES为你自己的Mysql数据库配置，在`/back-end-src`下依次运行`python manage.py makemigrations`和`python manage.py migrate`
3. 启动后台程序，命令行运行`python manage.py runserver`

## 3. 工具脚本说明：

①`tool_scripts/clean_useless_files.py`用于删除/media下已经失效的用户上传图片文件（完全没有被当前任何数据引用到的）；

②`tool_scripts/import_data.py`用于往数据表中插入预设数据（存放于`tool_scripts/data/wait_to_import`目录当中），用于初始化数据库；

③`tool_scripts/switch_setting.py`用于将`tool_scripts/data/db_backup`目录下制定文件（如`local.py`）替换到`APP_Inventor_case_base/settings.py`上

# 二、前端项目（front-end-src目录）

## 1. 架构说明

1. 项目整体使用TypeScript（它是JavaScript的一个超集，而且本质上向这个语言添加了可选的静态类型和基于类的面向对象编程）
2. webpack+Vue全家桶（①Vue2；②Vue-router；③axios；④Vuex）+Bootstrap3的前端项目框架（附注释）
3. 前端表单验证使用了1000hz-bootstrap-validator；文件上传使用了bootstrap-fileinput；富文本编辑使用了tinyMCE；图片编辑使用了cropper；轮播图使用了Owl-Carousel 2

## 2. 使用教程（下面的命令皆以front-end-src为当前目录运行）

1. 环境搭建。安装好`node.js`后，命令行运行`npm install`
2. 启动前端程序。命令行运行`npm run dev`
