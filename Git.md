# Git配置
* **初始配置**
  1. 设置全局用户名：打开git bash，输入`git config --global user.name "wenjie"`
  2. 设置全局邮箱：打开git bash，输入`git config --global user.email "x3011703521@163.com"`
* **查看配置**
  * 查看系统配置：`git config --system --list`
  * 查看用户全局配置：`git config --global --list`
* 配置ssh
  [参考文献](https://blog.csdn.net/weixin_44406127/article/details/137540031)
# Git创建本地仓库
1. 在目标目录下新建本地仓库文件夹
2. 在该文件夹下打开git bash
3. 运行指令 `git init`
***
# Git克隆远程仓库
1. 在目标目录下运行git bash
2. 运行指令 `git clone [url]`
***
# Git文件状态
* **untracked**：未跟踪，此文件在文件夹中，但没有加入git库不参与版本控制，此类文件可通过`git add`操作变为staged
* **unmodify**：文件已入库，此时版本库中文件快照内容与文件夹中内容一致，此类文件可被修改或通过`git rm`操作移出版本库
* **modified**：文件已修改，此类文件可通过`git add`操作进入暂存等待提交或通过`git checkout`操作从版本库中取出原版文件覆盖修改
* **staged**：暂存，此类文件可通过`git commit`操作提交至版本库，此时版本库中文件与本地文件一致，变为unmodify状态
***
# Git文件操作
* **查看文件状态**
  * 查看某一文件状态：`git status [filename]`
  * 查看所有文件状态：`git status`
  * 追踪所有文件：`git add .`
  * 提交暂存区文件到本地仓库：`git commit -m "提交信息"`
***
# Git忽略文件
在项目主目录下创建.gitignore文件，在文件中写忽略规则。
1. `*.txt` 忽略所有txt文件
2. `!lib.txt` 忽略lib.txt文件
3. `/test` 保留test文件夹忽略所有上级目录内容
4. `test/` 忽略test目录下的所有文件
5. `doc/*.txt` 忽略doc目录下的所有txt文件不包括该目录子文件夹下的txt文件
***
# Git分支 
* 列出所有本地分支：`git branch`
* 列出所有远程分支：`git branch -r`
* 列出所有本地分支和远程分支：`git branch -a`
* 新建一个分支，但依然停留在当前分支：`git branch [branch-name]`
* 新建一个分支，并切换到该分支：`git checkout -b [branch]`
* 新建一个分支，指向指定commit：`git branch [branch] [commit]`
* 新建一个分支，与指定的远程分支建立追踪关系：`git branch --track [branch] [remote-branch]`
* 切换到指定分支，并更新工作区：`git checkout [branch-name]`
* 切换到上一个分支：`git checkout -`
* 建立追踪关系，在现有分支与指定的远程分支之间：`git branch --set-upstream [branch] [remote-branch]`
* 合并指定分支到当前分支：`git merge [branch]`
* 选择一个commit，合并进当前分支：`git cherry-pick [commit]`
* 删除分支：`git branch -d [branch-name]`
* 删除远程分支:`git push origin --delete [branch-name]`或`git branch -dr [remote/branch]`
***
# GitHub使用技巧
## 搜索项目
在搜索框输入条件规则,可组合使用。[官方文档](https://docs.github.com/zh/search-github)
* 项目名称模糊查询：`in:spring boot`
* 限制条件大小查询：`stars:>2000`
* 限制条件范围查询：`stars:1000..2000`
* 限制日期：`created:>2016-04-29或pushed:<2019-07-05或created:2012-02-20..2018-08-30`
## 搜索关键词
* `awesome xxx`:xxx技术的著名项目大全
* `xxx sample`：找例子
* `xxx starter/xxx boilerplate`：找xxx技术的空项目架子
* `xxx tutorial`：找xxx技术的教程
***
