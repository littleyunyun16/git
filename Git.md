### Git使用

![](d:\Users\Desktop\2018122323213594.png)

* 创建项目的SSH Key

  1. 配置用户名：**git config --global user.name**  （github上注册的用户名

  2. 配置用户邮箱：**git config --global user.email**  （GitHub上注册时的邮箱）

     上面设置完成后可通过 Git config user.name  和git config user.email 来查看配置后的用户名和邮箱

  3. 在 Git终端输入**ssh-keygen -t rsa -C "youremail@example.com"*

  4. 创建完成后在用户主目录找到.ssh目录，里面有id_rsa和id_rsa.pub两个文件，这两个就是SSH Key的秘钥对，id_rsa是私钥，不能泄露出去，id_rsa.pub是公钥，可以放心地告诉任何人

  5. 登录[github](https://github.com/)注册或登录账号，打开“settings”的“SSH Keys”页面，然后，点“New SSH Key”，填上任意Title，在Key文本框里粘贴id_rsa.pub文件的内容，点“Add Key”，你就应该看到已经添加的Key

* 在本地创建个仓库，将本地内容上传到

  * 新建个仓库：可直接在网页上设置。

  * 复制仓库的ssh地址（不要复制https地址，踩过坑）

    关联远程库

    ```git
    $ git remote add origin git@github.com:michaelliao/learngit.git
    ```
  
  查看是否关联上： git *remote -v*  
  
  * 在d盘上新建文件夹（或者将本地仓库克隆到本地去）
    
    * cd /d  进入d盘
  * mkdir 创建本地GitHub文件夹
  * 将GitHub上的仓库克隆到本地 Git clone ssh 地址
  
  * 从本地上传文件到GitHub上
  * git add    将工作区创建的文件添加到暂存区
    * git commit  -m " 测试"   将暂存区的内容提交到仓库区
  * git push origin master  将仓库区的内容推送到远程仓库Github上
  
  

* 将Github的仓库克隆到本地来
* 将本地仓库修改提交到Github仓库
  * git status    查看仓库当前的状态，是否有被修改过
  * git diff   查看具体被修改的内容  按q退出
  * 若有修改 可以通过git add .      git  add   commit  -m  “ ”

*  版本回退
* 



lilux语句

https://www.cnblogs.com/zhuzhiwei-2019/p/10951141.html

* ls   查看当前目录下有什么文件和文件夹

  | 选项               | 含义                                                         |
  | ------------------ | ------------------------------------------------------------ |
  | -a                 | 列举目录中的全部文件，包括隐藏文件                           |
  | -l                 | 列举目录中的细节，包括权限、所有者、组群、大小、创建日期、文件是否是链接等 |
  | -f                 | 列举的文件显示文件类型                                       |
  | -r                 | 逆向，从后向前地列举目录中内容                               |
  | -R                 | 递归，该选项递归地列举当前目录下所有子目录内的内容           |
  | -s                 | 大小，按文件大小排序                                         |
  | -h                 | 以人类可读的方式显示文件的大小，如用K、M、G作单位            |
  | ls -l examples.doc | 列举文件examples.doc的所有信息                               |

* cd   

  * cd  文件路径  ：进入到该文件目录
  * cd   进入根目录
  * cd ../    返回上一目录

* mkdir    创建文件夹

* touch  创建文件

* 删除   rm -f    rm-rf

* cp 文件

* mv 移动文件

* vim 打开txt文件编辑

* cat 查看txt文件

* find/name文件检索

  















#### 碰到的问题



* git add test.txt 将工作区文件添加到暂存区，报错如下：

  解决方法：是因为unix系统与windows系统跨平台问题导致，执行git config core.autocrlf false后，再提交就不会报错了。

* push 到GitHub时，每次都要登录GitHub

https://blog.csdn.net/gatieme/article/details/45033349





