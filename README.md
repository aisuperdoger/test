# GladosAutoCheck

用法：

一、首先将该项目Fork到自己的仓库

![image-20220206030803688](D:\GladosAutoCheck\doc\image-20220206030803688.png)

二、然后到仓库的setting--Secret--Action页面处添加两个secret，分别命名为KOA_SESS与KOA_SESS_SIG，其值分别对应glados账号的两个cookie值

![image-20220206025252121](D:\GladosAutoCheck\doc\image-20220206025252121.png)

获取方法如下，

以edge浏览器为例，其他浏览器大同小异。登录账户后，F12进入应用程序栏，如下图点击获取两个cookie值

![image-20220206030120764](D:\GladosAutoCheck\doc\image-20220206030120764.png)

填完secret值后，在自己仓库点亮star即可开始运行

![image-20220206031659058](D:\GladosAutoCheck\doc\image-20220206031659058.png)



运行效果如下图

![image-20220206032210655](D:\GladosAutoCheck\doc\image-20220206032210655.png)

另外该脚本会在每天早上5点运行一次，需要修改运行事件可以把./.github/workflows/gladosCheck.yml的第八行

```
- cron: '0 21 * * *'    //国际时间
```

修改数字即可

