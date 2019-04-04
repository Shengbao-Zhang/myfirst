1.登陆GitHub
2.创建repository（仓库）
3.git绑定用户
	$ git config --global user.name "name"
	$ git config --global user.email xxxx@qq.com
4.设置ssh key
	4-1 生成ssh key
		先检查是否存在  $ cd ~/.ssh
		如果不存在     $ ssh-keygen -t rsa -C  "xxxx@qq.com"
	4-2 在GitHub上添加ssh key（new ssh key）
		Title:对应本地文件夹
		key:C:\Users\username\.ssh粘贴密钥
5.上传本地项目到GitHub
	5-1 在本地创建同名文件夹，各文件夹里边不能为空
	5-2 建立本地仓库
		git init //把这个目录变成Git可以管理的仓库
　　		git add README.md //文件添加到仓库
　　		git add . //不但可以跟单一文件，还可以跟通配符，更可以跟目录。一个点就把当前目录下所有未追踪的文件全部add了 
　　		git commit -m "first commit" //把文件提交到仓库，双引号内是提交注释。
　　		git remote add origin git@github.com:xxxx/xxxx.git //关联远程仓库
		如果上一步远程仓库关联错误，可以$ git remote rm origin之后重新关联
　　		git push -u origin master //把本地库的所有内容推送到远程库上
6.更新本地项目到远程库
	6-1 git add .
	6-2 git commit -m 'first commit'
	6-3 git remote add origin 你的远程库地址
	6-4 如果远程库不为空：git pull --rebase origin master
	6-5 git push -u origin master
