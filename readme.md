##这是第一个实现的功能

 ##初始化
	git init  （生成.git隐藏目录）
 
## 用户信息配置
	git config --global  user.name "lyz"
	git config --global  user.email "yuanzhenglu@126.com"
 
 ##
	git add ./readme.md      打开git仓库门 指定文件放在门口
	git commit -m "我们完成了第一个功能！"   提交代码，-m "message"并给出提示信息

##这是第二个实现的功能
	 git status  
	 查看当前状态，有没有放到仓储门外，没有的话，提示红色，有的话提示绿色。没有修改提示
	 On branch master nothing to commit, working tree clean

##这是第三个实现的功能

##这是第四个实现的功能
入口文件创建  index.js

##这是第五个个实现的功能
##  一次多个文件传送，当前目录下的更改的所有文件
	git add ./ e.md
	git commit --all -m "一次性操作"