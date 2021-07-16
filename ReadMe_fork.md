

解决原仓库 ReferenceError: primordials is not defined 的问题

https://stackoverflow.com/questions/55921442/how-to-fix-referenceerror-primordials-is-not-defined-in-node-js



对于github上的fork过的项目有更新，之前一直都是删除原来的fork然后重新fork解决的。。正确的更新姿势其实是这样，分享给有需要的朋友

```
git remote add upstream git@github.com:xxxx/xxx.git
git fetch upstream
git merge upstream/master
git push
```



记录下如何获取远程代码更新

没有找到界面工具，使用git命令操作，
IntelliJ IDEA 打开Terminal窗口

确定一下是否建立了主repo的远程源：
git remote -v

如果没有upstream, 则添加：
git remote add upstream url

从远程获取更新：
git fetch upstream

切换到本地分支：
git check main(我的本地分支名)

同步远程改动到本地：
git merge upstream/main

提交本地分支到我们自己fork仓库的远程服务器：
git push origin main

参考链接：

https://www.cnblogs.com/zhishaofei/archive/2004/01/13/9600580.html

https://www.cnblogs.com/haoyul/p/10512830.html
————————————————
版权声明：本文为CSDN博主「白话IT」的原创文章，遵循CC 4.0 BY-SA版权协议，转载请附上原文出处链接及本声明。
原文链接：https://blog.csdn.net/Jerry_Liangwn/article/details/109555306