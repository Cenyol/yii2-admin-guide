
###1、安装
这个就不说了，还是比较简单的。通过composer来，见：https://github.com/mdmsoft/yii2-admin

如果国内的小伙伴觉得composer慢得跟便秘一样的话，有方法的：http://pkg.phpcomposer.com


###2、路由
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
都听我讲，你第一步需要做的就是进入以上的第二个页面admin/route，这里会列出一些你已经开发好的controller/action，左边是系统全部的action，包括debug，gii这些路人都会出现在这里，而你开发的比如site里的，或者building里面的才是你之后需要控制分配的功能，选择他们，点击中间那个向右的按钮，这样它们才能在之后进行角色的权限分配和控制。
