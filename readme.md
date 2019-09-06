##这是第一个实现的功能

 ##初始化
	git init  （生成.git隐藏目录）
 
## 用户信息配置
	git config --global  user.name "lsername"
	git config --global  user.email "email-adress"
 
 ##
	git add ./readme.md      打开git仓库门 指定文件放在门口
	git commit -m "我们完成了第一个功能！"   提交代码，-m "message"并给出提示信息

##这是第二个实现的功能
	 git status  
	 查看当前状态，有没有放到仓储门外，没有的话，提示红色，有的话提示绿色。没有修改提示
	 On branch master nothing to commit, working tree clean
 
##  这是第三个实现的功能

##  这是第四个实现的功能
	入口文件创建  index.js

## 这是第五个个实现的功能
##  一次多个文件传送，当前目录下的更改的所有文件
	git add . 
	git commit --all -m "一次性操作"
	
##  查看日志信息
	git log
	git log --oneline
	
## 这是个回滚测试
	git reset --hard Head~0      		//回滚到哪里Head~0 最近一次提交，以此类推
	git reset --hard Head 字符串版本号  	//回滚到哪里Head~0 最近一次提交，以此类推
	git reflog  						//可以查看每次切换版本的记录

## 分支
	git branch  dev  				创建分支
	git branch  	  				查看分支
	git checkout dev 	  			切换分支
	git checkout master 	  		切换回来主支
	git merge dev 	  				合并分支到主支
	
	git branch -d dev				删除dev分支
	
## GitHub  https://github.com (git服务器)
	git push https://github.com/lyzlove/testdemo.git master
	

