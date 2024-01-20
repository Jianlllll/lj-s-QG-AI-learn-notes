# 基本命令

- 查看系统config  `git config --system --list`

- 查看当前用户（global）配置git `config --global  --list`

- `clone`: 克隆远程仓库到本地。

- `status`: 查看当前工作区的状态。

- `commit -m "ps"`: 提交暂存区中的更改，并添加提交信息。

- `add .`: 将当前工作区的所有文件添加到暂存区。

- `git push --force`

- `ssh-keygen -t rsa`创建

  `git remote add `关联

  `git remote rm origin` 删除

- 建立ssh连接的时候提示 connection refused ，详细建立ssh连接的过程可以使用 ssh -v 命令， -v 表示verbose，会打出详细日志.

  $ ssh -vT git@github.com

- ```
  列出所有本地分支git branch
  列出所有远程分支git branch -r
  新建一个分支，但依然停留在当前分支
  git branch [branch-name]
  新建一个分支，并切换到该分支
  git checkout -b [branch]
  合并指定分支到当前分支
  $ git merge [branch]
  删除分支
  $ git branch -d [branch-name]
  删除远程分支
  $ git push origin --delete [branch-name]
  $ git branch -dr [remote/branch]
  ```

# 配置命令

- 名称 **git config --global user.name ""**  
- 邮箱 **git config --global user.email** 

## 遇到的问题及解决方案

1，*cloning into 'test1'.fatal: unable to access*
*6 git clone https://github.com/i...*

*connect to host github.com port 22: connection refused*

解决方案 修改Windows本地hosts文件，定义IP地址和主机名的映射关系。

2*，fatal: The current branch main has no upstream branchTo push the current branch and set the remote as upstream*

 解决方案 git push --set-upstream github main

​	



## 基本知识

- ***文件的四种状态*** Untracked，Unmodify，Modified，Staged

- ***查看到文件的状态***  

  查看指定文件状态git status [filename]

  查看所有文件状态git status

- **忽略文件**

  ```
  *.txt        #忽略所有 .txt结尾的文件
  !lib.txt     #但lib.txt除外
  /temp     #向前忽略
  tempbuild/       #向后忽略
  ```

- clone和push的两种选择  ssh和https。在push时，前者需要管理员添加key（需要使用ssh-keygen先创建密钥对，再上传公钥到代码服务器），后者需要账号密码。
- ![image-20240118191848092](https://s2.loli.net/2024/01/18/dHsZAJko6bQ3w1T.png)
- ![image-20240118191854034](https://s2.loli.net/2024/01/18/T3racqnFvugjd71.png)

### 其他内容知识

- [Git 远程仓库(Github) | 菜鸟教程 (runoob.com)](https://www.runoob.com/git/git-remote-repo.html)

- [分支管理 - 廖雪峰的官方网站 (liaoxuefeng.com)](https://www.liaoxuefeng.com/wiki/896043488029600/896954848507552)

- [Git使用教程-KuangStudy-文章](https://www.kuangstudy.com/bbs/1707321856795000833)

- ipconfig /flushdns

  这将清除本地DNS缓存，使修改后的hosts文件生效。