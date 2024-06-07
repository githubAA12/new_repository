# Github
## 关键字查询

awesome,去标签类别中查询项目<br>python tutorial,查询资料，书籍，文档<br>
socket sample,查询对应的技术的代码样本


## github三要素
###  Repository 仓库

仓库是github项目管理储存的基本单位<br>
一个仓库中存储一个项目，一个用户可以拥有多个仓库，一般仓库分为public，private
### Commit提交
程序员在整个开发周期，有大量的对代码资源的迭代和修改，都可以通过commit的方式进行记录, 便于程序员回溯代码，即是这些代码被删除<br>
提交便于使用者观察整个工程的开发流程以及设计流程
### Branch分支
在仓库中可以包含多个分支，分支才是代码文件的第一存储单位，默认的仓库主分支为master/main<br>
不仅可以管理代码存储，便于多人协作开发<br>
![分支](https://s21.ax1x.com/2024/06/07/pkt8YAf.png "图片")
## 仓库内容
Code，资源存储，代码资源，二进制，项目管理脚本，许可证等等<br>
issues，使用时遇到的bug或进行提交，等待反馈<br>
README，使用markdown语言编写，工程自述文件，开发进度，版本更新，使用介绍等等
LICENSE 许可证<br>
GPL2.0,3.0.Apahce2.0,Mit，这些许可证，给使用者最大使用权限以及最少的限制
## Git软件，分布式版本控制系统
仓库管理软件，使用git管理私人代码或企业代码<br>
![仓库管理软件](https://s21.ax1x.com/2024/06/07/pkt8Dun.png "图片")
## 设备认证
1.如何让网站的账户与设备绑定，后续完成代码的管理，上传下载<br>
```bash
    git init //创建本地仓库 后续对仓库的操作，都要在仓库位置(master)
    git config --list //查看git的配置文件
    git config --global user.email "邮箱"
    git config --global user.name "用户名"
    ssh-keygen -t rsa -C "注册邮箱"  //创建本地密文
    去对应的目录查找密文文件
    rsa.pub 复制密文, 粘贴 settings -> SSH key and GPG -> new ssh key ->粘贴
    ssh -T git@github.com //测试关联是否成功
```
2.为目标仓库起别名，定位目标仓库，后续上传<br>
```bash
    git remote add origin "ssh地址" //为ssh仓库地址创建别名为origin 
    git remote remove origin //删除origin别名
    git remote add origin "ssh地址" //为ssh仓库地址创建别名为origin
```
## 本地设备与云端仓库的交互逻辑
![本地设备与云端仓库的交互逻辑](https://s21.ax1x.com/2024/06/07/pkt8rBq.png "图片")
## 代码更新的依赖关系被破坏
本地内容要比云端新，完成更新替换，但是如果直接修改云内容，导致，本地内容无法再次提交<br>
先拉取 git pull 云端内容 与本地内容合井或操作，而后再次推即可
```bash
    git pull --rebase origin maste
    git rebase --skip “忽酪本地内容 保留云端内容”
    git rebase --abort “忽駱本地内容 保留云端内容”
    git rebase --continue “忽駱本她内容 保留云端内容”
```
## 下载开源代码
```bash
    git clone "http下载地址"
```
##Markdown 语言
github可以编写readme，文本修饰语言
![Markdown](https://s21.ax1x.com/2024/06/07/pkt8RCF.png "图片")
