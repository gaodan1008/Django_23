##  一、本地配置环境 ##

1、在github服务器中创造仓库；
![](http://qmrc945r4.hn-bkt.clouddn.com/1-1.png)

2、在本地git bash中命令行中运行命令生成公私钥对ssh-keygen；

3、将 ~/.ssh/id_rsa.pub文件的内容复制到git服务器的ssh私钥中；
![](http://qmrc945r4.hn-bkt.clouddn.com/1-3.png)


4、新建repos文件夹放仓库；
	
	mikdir repos

5、git clone服务器中的仓库地址到本机；

	git clone git@github.com:gaodan1008/Django_23.git

5、cd仓库名目录，准备开始后面的编码工作；

	cd Django_23

6、在Git Bush中增加文件：readme.ms；增加app：news、polls；
	
	echo "作业">>readme.md

7、完成个人信息认证；
	
	git config --global user.eamail "820506157@qq.com"
	git config --global user.name "gaodan1008"

8、更新文件、检查文件、提交到本地仓库并注释、将文件push到github中的仓库。
	
	git add .
	git status
	git commit -m""
	git push

## 二、编写Django应用 ##

1、参考文献:编写你的第一个Django应用;

	https://docs.djangoproject.com/zh-hans/2.0/intro/tutorial01/
![](http://qmrc945r4.hn-bkt.clouddn.com/2-1.png)

2、在Visual Studio Code中编码，创建gitignore文件屏蔽pyc文件，下载sqlite插件并创建数据库sqlite3；

`**.pyc`
![](http://qmrc945r4.hn-bkt.clouddn.com/2-2.png)

3、在news目录下编写admin.py文件，创建superuser的账号，建立数据管理页面；

4、通过数据迁移命令将数据迁移到数据库；

	python manage.py migrate

5、在news目录下编写models.py、views.py、templates文件，创建网页展示界面；

6、在news目录下编写urls.py文件，提供网页地址；

	http://localhost:8000/news/articles/2020/
![](http://qmrc945r4.hn-bkt.clouddn.com/2-6.png)

7、在news目录下更新各个py文件增加上传的类HomeworkCreate，新建一个具有秒传功能的云盘系统（没有homework的表单）；
![](http://qmrc945r4.hn-bkt.clouddn.com/2-7.png)

8、更新文件、检查文件、提交到本地仓库并注释、将文件push到github中的仓库；
	
	git add .
	git status
	git commit -m""
	git push

9、启动服务器；
	
	python manage.py runserver
![](http://qmrc945r4.hn-bkt.clouddn.com/2-9.png)

10、用浏览器登录localhost:8000/admin查询网页界面。
	
	localhost:8000/admin
![](http://qmrc945r4.hn-bkt.clouddn.com/2-10.png)




