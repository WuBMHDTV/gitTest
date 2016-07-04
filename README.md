gitHelp
=======

### 注册一个github账号 ###

打开github主页，注册一个账号。

### 安装客户端 ###

在windows下，又不愿意用命令行，可以安装github自带的客户端，地址在[这里](http://windows.github.com/)，下载安装好以后，就像其他软件一样打开，然后用你的用户名登陆就行了。这时，可以看到在你的用户名下全部的项目，点击项目的clone可以克隆到本地进行编辑和提交。

### 找到你关注的项目 ###

这里，我们可以找到项目地址：[https://github.com/WuBMHDTV/gitTest](https://github.com/WuBMHDTV/gitTest)，然后点击页面右上角的 **“fork”** 按钮，这样就把你关注的项目fork到你自己的账号下了。  
此时你打开之前的客户端，在你自己的账户下就看到刚刚fork的项目了，然后点clone，把项目克隆到本地，克隆完以后可以在 **repositories** 标签中看到这个项目。右键点击可以打开项目的目录所在地。

### 修改你的项目 ###
在项目的本地克隆中修改你想修改的任何地方，添加，删除，修改文件都可以。比如在homework下建立一个自己github名字的[.md文件](http://baike.baidu.com/view/2311114.htm)

### 提交你的修改 ###
全部修改好了以后，打开github的客户端，在 **repositories** 标签找到刚刚的项目名称，点击名称右边的箭头，会出现你刚刚添加修改的内容，在右边填写提交说明，然后点 **commit** 进行提交，点完记得点上面的 *sync* 按钮，同步到github上，此时，打开你的github页面，就会出现你刚刚提交成功的内容。

### 发起一个pull request ###

提交完成以后，我们需要把我们的修改合并到[gitHelp](https://github.com/WuBMHDTV/gitTest)中，打开你自己的gitHelp项目克隆，地址是 [https://github.com/XXXXXX/gitTest](https://github.com/XXXXXX/gitTest)，点击上的 **Pull Request** 按钮，然后填写一些提交的信息，完成


### 将源作者的修改同步到你自己的github账户上 ###

如果你发现原作者已经修改了很多地方，你的代码和对方不同步了，此时需要将对方的代码同步到你的账户下，选择你自己账户下的repo，然后还是想发起pull request一样，点击 **Pull Request** 按钮，然后把左边改成你自己的项目，右边改成源作者的项目（之前是相反的），然后提交，提交完了以后会在你自己项目的pull request标签下显示出有项目提交了，此时点击 **merge pull request** 进行合并，如果没有冲突的话，会把对方的修改和你的修改合并到一起，如果有冲突需要进行手动合并，合并代码的时候请一定检查是否会影响你自己的代码。

###TEST###
很好的教程
谢谢
