- 本文是使用Github和git的简单入门教程，适用于从零开始学习Github的新手。
- 主要讲解如何将所做的项目文件上传到Github中，并从Github中下载项目。
## 一.什么是GitHub和Git？
- &emsp;&emsp;github是一个非常适合程序员交流的网站，很多国际上的技术大牛都在github上有自己的开源代码，其他人只要申请个账号就可以随意的看到这些大牛写的程序。同时国内的很多互联网公司如百度，阿里等，也在github上公布有开源的代码。  
- &emsp;&emsp;git是一个版本管理工具，是可以在你电脑不联网的情况下，只在本地使用的一个版本管理工具，其作用就是可以让你更好的管理你的程序。  
&emsp;&emsp;在做项目文件管理时，我们可以使用windows系统中一个非常消耗磁盘空间的方法。创建一个文件存储我们项目的代码，命名“项目1.0”，每次更新后，我们另外创建一个“项目2.0”，以此类推，但是在多人协作共同完成一个项目时，该方法存在问题：若程序员A修改了代码某一行，而B修改了另外一行，这两个版本的文件合并时，步骤非常复杂繁琐，而git的项目管理方式（分支、合并...）可有效解决上述问题。  

## 二.创建自己的Github账号并安装git
&emsp;&emsp;创建Github账号和git的方式在百度、谷歌、CSDN、知乎等网站搜索均有[相关教程](https://www.zhihu.com/question/20070065/answer/1879847761) 。

## 三.Git常用命令

### **1.git init**  
&emsp;&emsp;初始化创建仓库。  

### **2.git status**  
&emsp;&emsp;查看目前仓库的状态。  
  
### **3.git branch**  
&emsp;&emsp;查看分支，若需创建名为a的分支则，git branch a；若要删除a则git branch -d a  
  
### **4.git add .**  
&emsp;&emsp;添加所有文件到暂存区，若需要提交某个文件则将“.”改为“文件名+后缀”如"helloworld.txt"  
  
### **5.git commit -m “your message such as first commit”**  
&emsp;&emsp;将暂存区内容添加到本地仓库。  
  
### **6.git remote add + origin + URL**  
&emsp;&emsp;关联本地仓库和远程仓库，仓库名一般命名为origin，链接地址是Github上的URL，建议采用SSH协议。[SSH密钥介绍](https://zhuanlan.zhihu.com/p/134349361)  
  
### **7.git pull origin maste**  
&emsp;&emsp;从远程仓库下载（拉）更新内容,并立即将对应内容更新到本地仓库  
  
### **8.git push origin maste**  
&emsp;&emsp;将本地仓库内容上传（push）到远程仓库  
  
### **9.git merge**  
&emsp;&emsp;[分支合并](https://zhuanlan.zhihu.com/p/149287658)，不同的分支代表不同版本的修改，此命令对项目的版本进行更新，使项目保持最新。

### **10.git clone URL**  
&emsp;&emsp;将远程仓库的项目复制一份，保存到本地仓库，且两个项目间无关联。

&emsp;&emsp;（注：github更新后主分支名字由master更名为main）  
## 四.Windows下使用git上传本地项目
#### 1.在windows某盘创建空文件夹并命名，如“Introduction of github”。  
![图片1](picture/intro.jpg)  
#### 2.在文件夹Introduction of github文件中添加需要上传的项目如“hellogithub.txt”，建议其中有“README.md”。  
#### 3.在文件夹Introduction of github中，右键点击“Git Bash”，输入下列命令创建仓库。  
![图片1](picture/gitbash.jpg)  
`$ git init`  
#### 4.将本地文件添加到暂存区。  
`$ git add .`  
![图片1](picture/gitadd.jpg)  
#### 5.将暂存区内容添加到本地仓库(注意引号的中英文)  
`$ git commit -m "first commit"`  
#### 6.将本地仓库与远程仓库关联  
`$ git remote add origin URL`  
例如本文URL为：git@github.com:hkevin29/Introduction-of-github.git  
此时可以用git remote -v查看结果  
#### 7.将本地仓库内容上传到远程仓库。因是个人项目，没有多人协作，直接push；若多人协作则需要先git pull origin master，”commit-pull-push“三连的操作方式防止覆盖。  
`$ git push origin master`  
  

