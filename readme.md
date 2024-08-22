hello world

## Git Bash使用简单教程

##### 1. 设置用户

给电脑设置一个用户，上传的时候告诉远程仓库是谁上传的

`git config --global user.name "Your Name"`

`git config --global user.email "230248502@seu.edu.cn"`

##### 2. 仓库设置

把本地代码放到远程仓库

###### 初始化本地仓库

在建立本地仓库的文件夹中打开Git Bash，输入`$ git init`

###### 新建远程仓库

新建远程仓库在`github`上完成

###### 建立本地仓库和远程仓库之间的连接

1. 配置`SSH`

   1. 用`~/.ssh`或者用`~/.ssh ls`检查本地有没有`ssh`
   2. 用`$ ssh-keygen -t rsa -C "230248502@seu.edu.cn"`创建`SSH Key`
   3. 创建成功后会显示：

   **Your identification has been saved in /c/Users/user/.ssh/id_rsa**

   **Your public key has been saved in /c/Users/user/.ssh/id_rsa.pub**

2. 添加`SSH Key`到`GitHub`

   在`Github`的`Settings`里，建立新的`SSH Key`，在`Key`中输入`id_rsa.pub`下的全部内容

   可以使用`$ ssh -T git@github.com`

3. 在本地仓库中打开Git Bash，并建立链接

   `$ git remote add + 名字 + 自己的SSH链接地址`

4. 用`$ git remote -v`来检查

   **origin  git@github.com:SEUBridge/ESM.git (fetch)**
   **origin  git@github.com:SEUBridge/ESM.git (push)**

###### 文件上传

1. `git add -A`将修改的文件添加到暂存区，该语句提交所有变化
2. `git commit -m "修改注释"`将当前暂存区的文件实际保存到远程仓库的历史记录之中。**给刚才`add`的内容加一个备注，上传到远程仓库之后，修改的文件后便会显示这个备注**

3. `git push -u 仓库名称 + 分支`
   - 仓库名称：添加链接时指定的仓库名称
   - 分支：不同的分支名称
4. 
