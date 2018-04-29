### 操作资源管理器  
	cd e:  \\进入e盘
	mkdir project-git  \\创建名为"project-git"的文件夹
	cd project-git  \\进入"project-git"文件夹中
	ls -a  \\查看文件夹下所有文件及文件夹
	cd ..   \\退出到上一层
### 创建和编辑文件

	vim file.txt  \\创建file.txt文件并进入编辑模式
	Ctrl+C    :wq  \\退出编辑模式 
	cat file.txt  \\查看file.txt文件的内容
### git 命令
	git init  \\git项目初始化
	git status  \\查看git项目文件的状态
	git add file.txt  \\将文件file.txt添加到暂存区
	git commit -m "XXXX"  \\将文件从暂存区移至本地版本库，XXXX为说明性文字
	git add -A  \\将所有文件添加到暂存区
	git rm 移除
### git 远程推送
	git remote add origin  \\web地址 建立网络连接
	git remote -v  \\查看push和pull（fetch）所对应的网络地址
	git push -u origin master  \\本地master主干分支推送到远程，第一次-u关联后面直接用git push就可以
	git push -u origin master --allow-unrelated-histories 

### git克隆项目到本地
	git clone web地址 项目名称    \\从远程克隆项目名称

### git远程拉取代码
	git pull origin master  \\从远程master拉取代码文件  
> 

	git fetch 从远程获得更新
	git  merge origin/master 将更新和本地合并

### git版本回退
	git reset --hard Head^1  回退前一个版本
	git reset --hard Head~2 回退前两个版本
	git reset --hard commitId 回退或向前到指定版本（commitId指定）
> 获得版本信息和commitId

	git log  \\获得详细的历史版本信息
	git log --pretty=oneline  \\获得版本信息的简明信息
	git reflog  \\获得历史版本信息和版本操作的历史信息

### git stash 区的操作命令
> 用来保存某一时刻的工作区和暂存区的项目状态

	git stash save 将当前的工作区和暂存区的项目状态保存到stash区
	git stash pop 从stash区恢复
### git 分支
	git branch  \\分支的相关命令
	git checkout  \\定位分支
	git merge  \\合并分支