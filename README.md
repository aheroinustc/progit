# progit
For learning Pro Git book, written by Scott Chacon and Ben Straub.

Version 2.1.15, 2018-07-27

基于中文版本学习，参考英文版本以及其他网络资源。


## 使用https协议推送

先在github上面创建一个空的`repo:progit`，无任何内容及分支。

然后，本地新建并初始化一个`repo:progit`，添加`Readme.md`和`LICENSE`文件并`commit`。

添加远程仓库，执行`git push -u`可以在推送的同时设置关联。

    git init
    git add README.md LICENSE
    git commit -m "first commit"
    git remote add origin https://github.com/aheroinustc/progit.git
    git push -u origin master
    
首次`push`时，因为采取的是https协议，会跳出github的登录验证，

因为众所周知的原因，需要挂上代理登录，

如果有开启账户二次验证，请输入验证码。

可以在Github设置/Developer settings/Personal access tokens中管理访问授权，

需要时删除无效的tokens。

以后可以在本地继续提交，下次推送时，直接执行`git push`即可，

基本上不需要代理即可成功推送。

## 使用ssh协议推送(默认)

**添加SSH keys到github账户：**

``` bash
    $ git config --global user.name   "Your UserName"
    $ git config --global user.email  "Your Email"
    $ ssh-keygen -t rsa -C  "Your Email"
    $ cat  ~/.ssh/id_rsa.pub
```
默认在用户主目录`.ssh`下生成一对key。

将查看的`id_rsa.pub`内容复制，添加到github上的SSH keys。

命令行输入

    $ ssh -T git@github.com

如果出现如下信息则代表成功：

    Hi xxx! You've successfully authenticated, but GitHub does not provide shell access.

同样在github上面创建一个空的`repo:progit`，无任何内容及分支。

然后，本地新建并初始化一个`repo:progit`，添加`Readme.md`和`LICENSE`文件并`commit`。

添加远程仓库，执行`git push -u`可以在推送的同时设置关联。

    git init
    git add README.md LICENSE
    git commit -m "first commit"
    git remote add origin git@github.com:aheroinustc/progit.git
    git push -u origin master
    
以后可以在本地继续提交，下次推送时，直接执行`git push`即可，

基本上不需要代理即可成功推送。
