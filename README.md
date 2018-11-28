# Basement Django Template

Basement Django项目模板，用于开始一个新的Basement项目。使用步骤如下：

## 创建Django项目

首先，确保Django2.x已安装

使用以下命令创建一个新项目,并初始化git仓库：

```[language=shell]

$django-admin startproject --template=https://github.com/jeffkit/bsm-django-template/archive/master.zip project_name
$cd project_name
$git init

```

随后，添加一个git的子模块: bsm-django, 为bsm基础类库的django实现app：

```[language=shell]
git submodule add git@gitee.com:gitmen/bsm-django.git
```

添加完毕后，安装该子模块的依赖：

```[language=shell]
pip install -r bsm-django/requirements.txt
```

## 安装其他子模块

到此，新的BSM项目初始化完成。下面，可以有选择性的添加其他BSM的应用，如:bsm-member, bsm-cms,bsm-shop等,添加方式同样是以子模块的方式添加。它们对应的子模块地址为：

bsm-member: git@gitee.com:gitmen/bsm-member.git  用户的参考实现，通常建议默认安装，开发者可以继承member/User类进行扩展，亦可编写全新的用户类。
bsm-cms: git@gitee.com:gitmen/bsm-cms.git  内容管理应用
bsm-shop: git@gitee.com:gitmen/bsm-shop.git  在线商城应用
