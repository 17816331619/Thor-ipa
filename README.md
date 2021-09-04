# Thor-ipa
需要Thor的同学可以在这里找到ipa
ipa安装教程：https://www.i4.cn/news_detail_38195.html
顺带方舟防沉迷教程

打开Thor
点击蓝色小闪电上方的区域进入过滤器模块
新建过滤器名称请自便
依次进入挂载断点——编辑——新建中 的 命中条件：@req.url CONTAINS[cd] "ping"
并找到响应消息体回传前 中的
    判断条件：@req.url CONTAINS[cd] "ping"
    编辑——表达式(条件满足时)：^@rsp.bodyText "\{+.*\}$" "${response}"
回到主菜单找到 变量绑定——编辑——添加变量 中的
    变量名：response
    默认值：{"result":0,"message":"OK","interval":5400,"timeLeft":-1,"alertTime":600}
再次返回主菜单找到 包括域名   输入：as.hypergryph.com
进入   包括关键字   输入：/online/v1/ping
完成后回到主菜单
点击蓝色小火箭
会显示一个弹窗
点击   现在安装
跳转到Safari浏览器
会询问要不要安装  描述文件
点击  下载  或  安装
退出并进入设置
找到  通用——描述文件与设备管理——Thor SSL CA… ——选择右上角安装。
输入锁屏密码——右上角安装——弹窗提示选择安装
退出并找到  通用——关于本机——拉到最下面找到证书信任设置——针对根证书启用完全信任——继续
回到Thor，点击蓝色小闪电重新开始，如果没有弹窗就安装成功了
进到方舟试一下吧~(∩_∩)
