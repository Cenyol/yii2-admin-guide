
###1、安装（Install）
这个就不说了，还是比较简单的。通过composer来，见：https://github.com/mdmsoft/yii2-admin.如果墙内的小伙伴觉得composer慢得跟便秘一样的话，有方法的：http://pkg.phpcomposer.com


###2、路由（Route）
安装完，按照它说的，进入以下这几个页面你会发现啥也没有，或者说有些东西，但是一下子也不知道怎么用，毕竟原文guide没告诉你该怎么开始。
```
http://localhost/path/to/index.php?r=admin
http://localhost/path/to/index.php?r=admin/route
http://localhost/path/to/index.php?r=admin/permission
http://localhost/path/to/index.php?r=admin/menu
http://localhost/path/to/index.php?r=admin/role
http://localhost/path/to/index.php?r=admin/assignment
http://localhost/path/to/index.php?r=admin/user
```
都听我讲，你第一步需要做的就是进入以上的第二个页面admin/route，这里会列出一些你已经开发好的controller/action，左边是系统全部的action，包括debug，gii这些路人都会出现在这里，而你开发的比如site里的，或者building里面的才是你之后需要控制分配的功能，选择他们，点击中间那个向右的按钮，这样它们才能在之后进行角色的权限分配和控制。图的话，之前可以自己传的，不知道这次怎么找不到地方传了，借了张大概看下就行：
![](https://mdmunir.files.wordpress.com/2016/03/image03.png?w=1070&h=642)
总之呢，把你待会想要分配给某些角色们的那些action都选过来，第一次没选好待会也可以再回来继续选，爱怎么选都行。

###3、角色（Role）
嗯，跟我来，去这个页面：
```
http://localhost/path/to/index.php?r=admin/role
```
此时这里也是没有东西，你进去给我建几个角色，角色可以互相继承的。角色建好之后，是这样的，比如下面这图：（不能传图真不方便！）
图1占坑

