
# git���֪ʶ
## git��ʼ��
git init
## git ���Զ��վ��
git remote add origin [վ��λ��]
## ���git ����������û���
git config user.email "1105893943@qq.com" --global
git config user.name "zgdlzf"  --global
## ��ӻ���
git add .
git commit -m "�����Ϣ�Ĺؼ���"
## pull
git pull origin master
## push
git push origin master
## ɾ��git
rm -rf https://github.com/zgdlzf/GIT.git

# git�ֹ�����
## ��Ŀ����
���� / ���� / ���� ���㹲ͬЭ��������һ�ײ���ϵͳ
## ��Ŀ�ֹ���

���� / ���� ��������ϵͳ
���帺������ϵͳ
## �����������˲ֿ�
master
develop
master�����ȶ���(production ready)��������Աƽʱ�Ĵ��붼�ύ��develop��֧��
## �����ߵ�git��֧
������Git��֧
article (local)
lisi/article (via git remote add lisi http://lisi-server/lisi.git)
origin/develop (via git remote add origin http://remote-server/blog.git)
## ���ĵ�Git��֧

article (local)
zhangsan/article (via git remote add zhangsan http://zhangsan-server/zhangsan.git)
origin/develop (via git remote add origin http://remote-server/blog.git)
## �����Git��֧
comment (local)
origin/develop (via git remote add origin http://remote-server/blog.git)
## ��������
����������һ���ֺ�(n�α���commit)���ύ�����ص�git server(Ҳ����������ӵ�http://zhangsan-server/zhangsan.git)��

���Ŀ�����һ���ֺ���ΪҪ�����������Ĳ��ֺϲ���������Ҫִ��һ��rebase��merge
## ��ǰ��article��֧��
git rebase zhangsan/article
## �ύ�����ص�git server (Ҳ����������ӵ�http://lisi-server/lisi.git)��
git push local/article master
