# Git

## 安装

- Windows

  https://git-scm.com/downloads

> 下载太慢的解决方法

https://npm.taobao.org/mirrors/git-for-windows/

![image-20200630234725998](C:\Users\30934\AppData\Roaming\Typora\typora-user-images\image-20200630234725998.png)

> 下拉到最底部，可以看到最新版的git-for-windows

![image-20200630234818596](C:\Users\30934\AppData\Roaming\Typora\typora-user-images\image-20200630234818596.png)

> 点击下载64bit的，以exe结尾的文件

> 下载完成之后一路确认就行



## 配置

首次使用git

![image-20200701000226726](C:\Users\30934\AppData\Roaming\Typora\typora-user-images\image-20200701000226726.png)

```
git config --global user.name "Your Name"
git config --global user.email "email@example.com"
```



## 新建库示例

```
git init
git add .
git commit -m "something"
git remote add origin git@github.com:Duangi/deploysNotes.git
//origin后面是github中库的名字
git push -u origin master
```

