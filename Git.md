# Git

## 安装

- Windows

  https://git-scm.com/downloads

> 下载太慢的解决方法

https://npm.taobao.org/mirrors/git-for-windows/

![安装-1](https://raw.githubusercontent.com/Duangi/deploysNotes/master/Git.assets/安装-1.png)

> 下拉到最底部，可以看到最新版的git-for-windows

![安装-2](https://raw.githubusercontent.com/Duangi/deploysNotes/master/Git.assets/安装-2.png)

> 点击下载64bit的，以exe结尾的文件

> 下载完成之后一路确认就行



## 配置

首次使用git

![配置-1](https://raw.githubusercontent.com/Duangi/deploysNotes/master/Git.assets/%E9%85%8D%E7%BD%AE-1.png)

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

![push-1](https://raw.githubusercontent.com/Duangi/deploysNotes/master/Git.assets/push%E6%9D%83%E9%99%90-1.png)

> git会告诉你将文件保存在了哪里

> 将id_rsa.pub中的内容复制下来
>
> 打开github - settings界面 - SSH and GPG keys - new SSH keys
>
> title随便命名，再将刚刚复制的内容粘贴到里面，确认



## 上传带有图片的md文件

1. 将所有图片文件保存到文件夹里，上传到github上

   ![上传-1](D:\Material\Notes\deploysNotes\Git.assets\image-20200701100003913.png)

2. 点击对应的图片旁边的download按钮，记录下来图片的绝对url

   ![上传-2](D:\Material\Notes\deploysNotes\Git.assets\image-20200701100046955.png)

   ![上传-3](D:\Material\Notes\deploysNotes\Git.assets\image-20200701100120769.png)

3. 在md文件中修改图片的url为以下格式

   ```
   ![Image text](https://raw.githubusercontent.com/Duangi/deploysNotes/master/Git.assets/push%E6%9D%83%E9%99%90-1.png)
   ```

4. push

## github图片无法显示

如果在github中图裂了，可能是因为浏览器dns配置问题

修改C:\Windows\System32\drivers\etc里的hosts文件

在最后添加：

```
# GitHub Start 
140.82.113.3      github.com
140.82.114.20     gist.github.com

151.101.184.133    assets-cdn.github.com
151.101.184.133    raw.githubusercontent.com
151.101.184.133    gist.githubusercontent.com
151.101.184.133    cloud.githubusercontent.com
151.101.184.133    camo.githubusercontent.com
151.101.184.133    avatars0.githubusercontent.com
199.232.68.133     avatars0.githubusercontent.com
199.232.28.133     avatars1.githubusercontent.com
151.101.184.133    avatars1.githubusercontent.com
151.101.184.133    avatars2.githubusercontent.com
199.232.28.133     avatars2.githubusercontent.com
151.101.184.133    avatars3.githubusercontent.com
199.232.68.133     avatars3.githubusercontent.com
151.101.184.133    avatars4.githubusercontent.com
199.232.68.133     avatars4.githubusercontent.com
151.101.184.133    avatars5.githubusercontent.com
199.232.68.133     avatars5.githubusercontent.com
151.101.184.133    avatars6.githubusercontent.com
199.232.68.133     avatars6.githubusercontent.com
151.101.184.133    avatars7.githubusercontent.com
199.232.68.133     avatars7.githubusercontent.com
151.101.184.133    avatars8.githubusercontent.com
199.232.68.133     avatars8.githubusercontent.com

# GitHub End
```



## 无法修改hosts文件

https://zhidao.baidu.com/question/45783942.html