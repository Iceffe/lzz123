## 1.  下载 Git
【github新建库】
【建立SSH连接】
【git本地版本库】
【git-github 提交】

## 2.  github 新建库
![库栈.png](https://upload-images.jianshu.io/upload_images/8534714-3d2b4cba57681ad2.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)

## 3. 建立SSH连接通道
  1. 首选确认自己本机用户主目录下（/c/User/用户名字/）是否有存在.ssh目录，目录下是否存在id_rsa和id_rsa.pub两个文件，
  2. 没有 右键 **git bash here：**`ssh-keygen -t rsa -C "邮箱名字@xxx.com"`    通常一直回车
    ![ssh.png](https://upload-images.jianshu.io/upload_images/8534714-4ea7f2ee47de70bd.png?imageMogr2/auto-orient/strip%7CimageView2/2/w/1240)
  3. .ssh/known_hosts 生成这个文件  直接删除 重新生成就好了、
  4. github 添加ssh  **Key is already in use** 可能是相同邮箱秘钥  删除就好

##  4. 文件夹 Git Bash Here =>
```
 echo "# lzz123" >> README.md
 git init
 git add README.md
 git commit -m "first commit"
 --
 git remote add origin https://github.com/colzz/lzz123.git
 git push -u origin master
```

### 5. Git提交时显示用户 unknown
```
$ git config --global user.name "your_name"
$ git config --global user.email "your_email@youremail.com"
```
## ***
```
$ git push origin
```
上面命令表示，将当前分支推送到origin主机的对应分支。
如果当前分支只有一个追踪分支，那么主机名都可以省略。
```
$ git push
```
上面命令将本地的master分支推送到origin主机，同时指定origin为默认主机，后面就可以不加任何参数使用git push了。
```
$ git push -u origin master
```
不带任何参数的git push，默认只推送当前分支，这叫做simple方式。此外，还有一种matching方式，会推送所有有对应的远程分支的本地分支。Git 2.0版本之前，默认采用matching方法，现在改为默认采用simple方式。
