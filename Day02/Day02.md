# 1. windows系统下git的使用
## 1.下载Git Bash
进入Git Bash官网下载
https://git-scm.com/download/win
![gitbash](img/gitbash.png =x10)
gitbash打开后界面（后面推荐将git配置到win自带的terminal）
![[Pasted image 20230126125556.png]]
## 2.git配置到win自带终端cmd（推荐）
查看高级系统设置，选择环境变量
![[Pasted image 20230126134638.png]]
进入环境变量，选择Path，点击编辑
![[Pasted image 20230126134817.png]]
新建一个环境变量，为gitbash安装路径下的cmd文件夹
注意使用自己的安装路径而不是图中路径！！
![[Pasted image 20230126135215.png]]
确定后，打开cmd测试，出现git命令提示即为正常
![[Pasted image 20230126135320.png]]
## 3.git配置 
设置用户名和邮箱
```c++
git config --global user.name "用户名"

git config --global user.email "邮箱"
```
欧了
## 4.使用git创建一个库（不太聪明的方法）
略，用不到
## 5.使用ssh方法连接远程仓库（聪明的方法）
### 1.配置ssh密钥至github仓库
在cmd中配置好git的基础上，在cmd中输入下面的命令
务必更换成登录GitHub使用的邮箱
```shell
ssh-keygen -t ed25519 -C "your_email@example.com"
```
执行完后可以在图中路径找到ssh公钥文件id_rsa.pub
![[Pasted image 20230126142253.png]]
打开后即可看到ssh公钥
![[Pasted image 20230126142618.png]]
在任何页面的右上角，单击个人资料照片，然后单击“设置”。
    ![用户栏中的 Settings 图标](https://docs.github.com/assets/cb-34573/images/help/settings/userbar-account-settings.png)
在边栏的“访问”部分中，单击 “SSH 和 GPG 密钥”。
单击“新建 SSH 密钥”或“添加 SSH 密钥” 。![SSH 密钥按钮](https://docs.github.com/assets/cb-28257/images/help/settings/ssh-add-ssh-key-with-auth.png)
在 "Title"（标题）字段中，为新密钥添加描述性标签。 例如，如果使用的是个人笔记本电脑，则可以将此密钥称为“个人笔记本电脑”。  
将密钥粘贴到 "Key"（密钥）字段。![密钥字段](https://docs.github.com/assets/cb-47495/images/help/settings/ssh-key-paste-with-type.png)
单击“添加 SSH 密钥”。
![“添加密钥”按钮](https://docs.github.com/assets/cb-6592/images/help/settings/ssh-add-key.png)
### 2.克隆仓库到本地 
进入需要克隆的仓库，以Monica_C_plusplus仓库为例子
复制ssh协议的git链接
![[Pasted image 20230127124401.png]]
右键桌面，选择在终端中打开
![[Pasted image 20230127125541.png]]
进入终端，使用git clone命令，并在后面加入git链接
``` shell
git clone git@github.com:Que121/Monica_C_plusplus.git
```
![[Pasted image 20230127125657.png]]
回车后即可克隆仓库至本地
![[Pasted image 20230127130319.png]]
## 6.拉取仓库和更新仓库
## 1.拉取仓库
拉取仓库指将github仓库文件拉取到本地
拉取仓库十分简单
```shell
git pull
```
在仓库文件夹下右键打开终端
![[Pasted image 20230127130954.png]]
git pull然后回车
![[Pasted image 20230127131041.png]]
## 2.更新仓库
更新仓库指将本地仓库更新到github仓库，也叫push到github
在更新仓库前必须先拉取最新仓库进行合并
在仓库首目录按以下命令执行
```shell
git add .
```
![[Pasted image 20230127132754.png]]
“注释”为此次更新的备注信息，可更改
```shell
git commit -m "注释"
```
![[Pasted image 20230127133012.png]]
最后git push即可更新仓库
![[Pasted image 20230127133041.png]]
更新成功后，在github上看到更新结果
![[Pasted image 20230127133138.png]]
# 2. Obsidian的使用
官网下载obsidian
https://obsidian.md/
详细使用可参考
https://publish.obsidian.md/help-zh/Obsidian/Obsidian
最基本的使用，打开克隆到本地的仓库
![[Pasted image 20230127133813.png]]
即有这样的页面
![[Pasted image 20230127133942.png]]
编辑语法为markdown，使用ctrl+p可以调出帮助页面
![[Pasted image 20230127134144.png]]
图片过小，右键图片查看原图
![[Pasted image 20230127134249.png]]

