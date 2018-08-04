
# git相关知识
## git初始化
git init
## git 添加远程站点
git remote add origin [站点位置]
## 添加git 配置信箱和用户名
git config user.email "1105893943@qq.com" --global
git config user.name "zgdlzf"  --global
## 添加缓存
git add .
git commit -m "添加信息的关键词"
## pull
git pull origin master
## push
git push origin master
## 删除git
rm -rf https://github.com/zgdlzf/GIT.git

# git分工合作
## 项目背景
张三 / 李四 / 王五 打算共同协作，开发一套博客系统
## 项目分工：

张三 / 李四 负责文章系统
王五负责评论系统
## 建立服务器端仓库
master
develop
master保存稳定版(production ready)，开发人员平时的代码都提交到develop分支上
## 开发者的git分支
张三的Git分支
article (local)
lisi/article (via git remote add lisi http://lisi-server/lisi.git)
origin/develop (via git remote add origin http://remote-server/blog.git)
## 李四的Git分支

article (local)
zhangsan/article (via git remote add zhangsan http://zhangsan-server/zhangsan.git)
origin/develop (via git remote add origin http://remote-server/blog.git)
## 王五的Git分支
comment (local)
origin/develop (via git remote add origin http://remote-server/blog.git)
## 开发过程
张三开发完一部分后(n次本地commit)，提交到本地的git server(也就是李四添加的http://zhangsan-server/zhangsan.git)。

李四开发完一部分后，因为要与张三开发的部分合并，所以需要执行一下rebase或merge
## 当前在article分支中
git rebase zhangsan/article
## 提交到本地的git server (也就是张三添加的http://lisi-server/lisi.git)。
git push local/article master
