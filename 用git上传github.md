\1.   git init 把文件变成git可管理的仓库

![说明: C:\Users\Administrator\AppData\Local\Microsoft\Windows\INetCache\Content.Word\init.png](file:///C:\Users\ADMINI~1\AppData\Local\Temp\msohtmlclip1\01\clip_image001.png)

 

\2.   git add 项目**粘贴**到本地git仓库，可以使用git status查看当前状态

![说明: C:\Users\Administrator\AppData\Local\Microsoft\Windows\INetCache\Content.Word\add.png](file:///C:\Users\ADMINI~1\AppData\Local\Temp\msohtmlclip1\01\clip_image002.png)

 

\3.   git commit 把项目添加到本地仓库

注意：-m后面引号是本次提交的注释内容，最好写上，不然报错

![说明: C:\Users\Administrator\AppData\Local\Microsoft\Windows\INetCache\Content.Word\commit.png](file:///C:\Users\ADMINI~1\AppData\Local\Temp\msohtmlclip1\01\clip_image003.png)

\4.   创建SSH KEY 

a)    先看c盘目录下有没有.ssh目录，有的话看看有没有id_rsa和id_rsa.pub。有就跳到下一步，没有就执行下面命令

ssh-keygen -t rsa -C [邮箱名@qq.com](mailto:邮箱名@qq.com)   

![img](file:///C:\Users\ADMINI~1\AppData\Local\Temp\msohtmlclip1\01\clip_image004.png)

![img](file:///C:\Users\ADMINI~1\AppData\Local\Temp\msohtmlclip1\01\clip_image005.png)

b)    登录github，找如图，点击settings，再点击SSH and GPS KEYS，点击NEW SSH KEY,title随便填，把id_rsa.pub里的内容复制到key内容里，最后点击ADD SSH key，这就完成SSH key加密

![img](file:///C:\Users\ADMINI~1\AppData\Local\Temp\msohtmlclip1\01\clip_image006.png)

\5.   在github创建git仓库

直接点New repository来创建

 

\6.   在Github上创建好Git仓库之后我们就可以和本地仓库进行关联

git remote add origin 仓库的路径

![img](file:///C:\Users\ADMINI~1\AppData\Local\Temp\msohtmlclip1\01\clip_image004.png)

 

\7.   关联后可以推送到远程仓库

a)  新建远程仓库是空的，所以要加上-u :  git push -u origin master

<<<<<<< HEAD
<<<<<<< HEAD
b)  远程仓库有内容之后再从本地上传内容可以用 git push origin master
=======
<<<<<<< HEAD
b)  远程仓库有内容之后再从本地上传内容可以用 git push origin master
=======
b)  远程仓库有内容之后再从本地上传内容可以用 ：git push origin master
>>>>>>> 85b731b (ts内容)
>>>>>>> c22146f (ts)
=======
b)  远程仓库有内容之后再从本地上传内容可以用 git push origin master
>>>>>>> 71ab833d595a88aafa91349e39c3d05a73db86af

注意:上传项目的过程需要等待一段时间

![img](file:///C:\Users\ADMINI~1\AppData\Local\Temp\msohtmlclip1\01\clip_image007.png)

 

 

之后你的远程仓库就有内容了。。。。。

 

 

 

如果推送到有内容的远程仓库，报这样的错：error: failed to push some refs to “xxxx”

 那么使用  **git pull --rebase origin master ** 

 这命令是把远程仓库中更新合并到本地库中

**–-rebase**的作用是取消掉本地库中刚刚的commit，并把他们接到更新后的版本库之中

 

 

 

 

 

 

 

 

 

 

<<<<<<< HEAD
<<<<<<< HEAD
 
=======
<<<<<<< HEAD
 
=======
 给i他
>>>>>>> 85b731b (ts内容)
>>>>>>> c22146f (ts)
=======
 
>>>>>>> 71ab833d595a88aafa91349e39c3d05a73db86af
