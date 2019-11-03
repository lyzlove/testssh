## 初始化

	git init  （生成.git隐藏目录）
 
## 用户信息配置

	git config --global  user.name "lsername"
	git config --global  user.email "email-adress"
 
##  git add  / git commit  提交代码

	git add ./readme.md      打开git仓库门 指定文件放在门口
	git commit -m "我们完成了第一个功能！"   提交代码，-m "message"并给出提示信息

##  查看当前git状态

	 git status  
	 查看当前状态，有没有放到仓储门外，没有的话，提示红色，有的话提示绿色。没有修改提示
	 On branch master nothing to commit, working tree clean

##  一次多个文件传送，当前目录下的更改的所有文件
 
	git add ./          这里是你git所在位置的所有文件
	git commit --all -m "一次性操作"
	
##  查看日志信息

	git log        				查看操作日志信息，
	git log --oneline			查看简要的日志信息  -m信息和版本号
	
## 代码回滚操作

	git reset --hard Head~0      		//回滚到哪里Head~0 最近一次提交，以此类推
	git reset --hard Head 字符串版本号  	//回滚到哪里Head  字符串版本号
	git reflog  						//可以查看每次切换版本的记录

## 分支

	git branch  dev  				创建分支
	git branch  	  				查看分支
	git checkout dev 	  			切换分支
	git checkout master 	  		切换回来主支
	git merge dev 	  				合并分支到主支
	
	git branch -d dev				删除dev分支
	
## GitHub  https://github.com (git服务器)

	代码本地提交后，就可以去git服务器提交代码了
	git push 地址 master
		
##  从服务器下载代码
 
	新建一个文件夹  执行	git init 然后 git push
	git push 地址 		// 里面的master都是主分支，也可以其他分支
	
## git clone 克隆服务器项目内容

	git clone 地址 
	
	第一次下载代码的时候可以直接克隆一个和服务器完全一样的代码
	如果多次执行，每次都会把本地代码覆盖

## ssh 方式上传代码

	公钥，私钥 两种，首先生成两种钥匙  -t 加密方式 rsa
	ssh-keygen -t rsa  -C "邮箱地址"
	生成后再提示的生成地址中找到对应的公钥 id_rsa.pub, 文本打开复制里面的内容
	然后进入进入git 服务器，点击右上角的图标，下拉框进入setting
	然后设置 SSH and GPG keys ，新建 sshkey ,
	标题自己定义，下面输入从公钥总复制的内容，然后保存，
	保存后 download 中的use ssh 地址 就可以git push 上去了
	
	git push   ssh地址   master

##  代码提交的时候要先从服务器下载代码，以免服务器代码更新了，自己的还没有更新，造成版本冲突
	
	先 pull   
	后 push
	
##  服务器地址输入简化配置(用origin代替远程地址)
	
	git remote add origin git地址
	git push origin master
	
	git push origin  -u master  		//把本地的分支提交到服务器代码中
	git push 							//简化后只需要git push 就可以完成代码提交

## pull

	
