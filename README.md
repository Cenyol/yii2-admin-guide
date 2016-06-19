###1、安装（Install）
这个就不说了，还是比较简单的。通过composer来，见：https://github.com/mdmsoft/yii2-admin 如果墙内的小伙伴觉得composer慢得跟便秘一样的话，有方法的：http://pkg.phpcomposer.com


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
![](https://github.com/Cenyol/yii2-admin-guide/blob/master/1.png?raw=true)

眼光向右扫，可以看到那个小眼睛的图标，点进去查看。你看会看到左边是一个列表，左边是空空的。左边由Roles和Routes组成，前者是我们刚刚创建的角色，后者是我们第二步选择的那些action。就是在这里分配的。需要让哪些角色拥有哪些技能，就在该角色里面，将那些技能(action)选中，然后点击中间的绿色向右箭头即可。唠叨一句，左边那个可以使用shift来多选，或者直接鼠标拖动多选。
结果类似下面这样
![](https://github.com/Cenyol/yii2-admin-guide/blob/master/2.png?raw=true)

###4、分配(Assignment)
给用户分配角色，即让谁成为什么。比如我（cenyol），是我开发的系统的他爸，角色名叫：造物者。🤓
```
http://localhost/path/to/index.php?r=admin/assignment
```
此时，系统里必须得有几个用户注册好了才能分配。分配列表长这样：
![](https://github.com/Cenyol/yii2-admin-guide/blob/master/3.png?raw=true)
![](https://github.com/Cenyol/yii2-admin-guide/blob/master/4.png?raw=true)

###5、菜单(Menu)
这个功能很使用，就是把你想要显示在你导航栏的菜单项列出来，至少我是这么理解的也是这么做的，也如我所想。先来个图：![](https://github.com/Cenyol/yii2-admin-guide/blob/master/5.png?raw=true)

这是造物者这个角色的左侧导航栏显示的菜单。再登陆一下普通员工，截个图：
![](https://github.com/Cenyol/yii2-admin-guide/blob/master/6.png?raw=true)

对比他们的不同了吧，不一样的人，登陆进来之后，根据他们不同的权限，是可以在这里设置显示不同的菜单的。
```
http://localhost/path/to/index.php?r=admin/menu
```

嗯，基本初步使用这样就够了，有需要再更新，坐一整天脊椎快不行了，回去跑个步。