# Git

## 安装

- Windows

  https://git-scm.com/downloads

> 下载太慢的解决方法

https://npm.taobao.org/mirrors/git-for-windows/

![Image text]()

![image-20200630234725998](D:\Material\Notes\deploysNotes\Git.assets\image-20200630234725998.png)

> 下拉到最底部，可以看到最新版的git-for-windows

![image-20200630234818596](D:\Material\Notes\deploysNotes\Git.assets\image-20200630234818596.png)

> 点击下载64bit的，以exe结尾的文件

> 下载完成之后一路确认就行



## 配置

首次使用git

![image-20200701000226726](D:\Material\Notes\deploysNotes\Git.assets\image-20200701000226726.png)

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



## 给予push权限

> git bash中输入以下命令配置ssh key

```ssh-keygen -t rsa -C "youremail@example.com"```

>  将邮箱换成你自己的邮箱，一路回车

![image-20200701001553943](D:\Material\Notes\deploysNotes\Git.assets\image-20200701001553943.png)

> git会告诉你将文件保存在了哪里

> 将id_rsa.pub中的内容复制下来
>
> 打开github - settings界面 - SSH and GPG keys - new SSH keys
>
> title随便命名，再将刚刚复制的内容粘贴到里面，确认



## 上传带有图片的md文件

1. 将所有图片文件保存到文件夹里，上传到github上
2. 点击对应的图片旁边的download按钮，记录下来图片的绝对url