# Git 分布式版本控制系统

# 第一次安装
    git config --global user.name 'zwx'
    git config --global user.email 'zwx@aaa.com'
    --global指令后整台机器都使用该配置

# 创建版本库 repository
    在某目录下git init，该目录即变为Git可以管理的仓库。.git为Git用来跟踪管理版本库的。
    git add xxx/. 把文件添加到仓库
    git commit -m 'zwx' 把文件提交到仓库

# 状态查看
    git status 查看仓库当前状态
    git diff xxx 查看某文件的改动
    git log 显示从最近到最远提交的'zwx'

# 版本回退
    git reset --hard HEAD^ 回退到上个版本
    git push origin HEAD --force 强制将回退版本推送到远程
    git reset --hard commit_id 找到想要回退版本的commit_id即可
    git reset HEAD xxx 某文件版本回退

# 删除文件
    git rm xxx
    git commit -m 'zwx'

# 文件从版本库还原至工作区
    git checkout -- xxx 工作区文件被误删后，如已提交至版本库可找回

# github SSH设置
    github可以看做Git的服务器
    Git 和 github 之间的传输通过 SSH 加密
    ssh-keygen -t rsa -C "youremail@example.com" 生成id_rsa（私钥）和 id_rsa.pub（公钥）
    在github SSH Keys 中添加 id_rsa.pub 的内容
    不同电脑可设置多个SSH Keys

# 推送至github
    git remote add origin git@github.com:xxx/xxx 将本地仓库与github仓库关联
    已关联了某个远程库再重新关联其他时 git remote rm origin
    origin默认为远程库
    git push origin master 将当前分支master推送至远程库origin
    git push -f origin master 远程库存在文件时，会强制用提交的文件覆盖远程库
    远程库中已存在文件，使用前先 git pull origin master

# 克隆远程库
    git clone xxx



