## git版本管理 ##

git版本管理分为两个部分，一个是本地库，一个是远程库，不论在本地库还是远程库都可以进行管理，一般的操作是提交什么的都在本地库进行，当有可用的版本或者需要在另外的机器上同步的时候，可以将本地库提交到远程库上面去，然后别的机器就可以和你同步了。

### 初始化版本库 ###

初始化版本库一般有两种方法

1. `git clone` 这是一种较为简单的初始化方式，当你已经有一个远程的Git版本库，只需要在本地克隆一份,比如将远程库克隆一份到本地。
    > git  clone  git://github.com/XXX/some_project.git   some_project
2. `git init` 和 `git remote`：这种方式稍微复杂一些，当你本地创建了一个工作目录，你可以进入这个目录，使用`git init`命令进行初始化；Git以后就会对该目录下的文件进行版本控制，这时候如果你需要将它放到远程服务器上，可以在远程服务器上创建一个目录，并把可访问的URL记录下来，此时你就可以利用`git remote add`命令来增加一个远程服务器端，这样，你就建立了一个本地库和一个远程库。
    > git  remote  add  origin  git://github.com/someone/another_project.git


### 提交修改 ###

版本库建立好以后就可以增，删，修改目录下的任意文件了，修改完成以后就需要进行提交，提交分为两部分，建立提交索引和真正的提交。

- 建立提交索引，实际上就是告诉git你做了哪些修改，一般有 `git add`命令和`git rm`命令。
> git add .  #添加文件，'.'表示添加所有文件，也可以用文件名
> git rm some_file #删除文件


也可以使用 `git add -A \<path\>`将path中所有文件的修改，增加，删除添加到版本库索引中

- 提交代码，使用`git commit -m "some information"`，必须要使用-m参数来说明都提交了什么内容，可以用中文。

### 更新代码 ###

如果是多人操作一个版本库，有可能你在提交的时候别人也提交过了，这时需要更新代码库，使用`git pull`命令更新本地代码库。

由于我们使用的是`pull request`的开发模式，理论上你自己的代码库，不管是远程的还是本地的，都只有你一个人修改，只有当你认为你的修改ok了以后，才会使用**网页上的**`pull request`请求将修改同步到WuBMHDTV账户的主分支，所以一般在你自己的代码库上不存在冲突。

### 建立分支 ###

分支的含义自行google，git建立分支比较简单，分支也分为本地分支和远程分支

- 建立本地分支，`git branch [name]`，如果没有`name`参数，就是查看本地分支，建立好以后可以切换到新分支 `git checkout [name]`，以后你提交的代码就都在这个新分支了。
- 建立远程分支，`git push origin [name]`

### 将代码提交到远程版本库 ###

一般是做了一系列修改以后才会将代码提交到远程版本库。使用命令

>git push origin test:test  #将本地test分支推送到远程test分支
>git push origin master     #将当前分支推送到远程master分支

命令行基本操作就这些个，后面还有个代码回滚需要详细说明一下。