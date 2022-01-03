1.把master分支作为上传github的分支
git push --set-upstream origin master

2.把私钥与设置的公钥匹配核对
ssh -T git@github.com

3.查看公钥
cat ~/.ssh/id_rsa.pub

4.基于邮箱生成密钥
ssh-keygen -t rsa -C "xizhao.yh@gmail.com"

5.查看密钥有无
切换到目录 ～/.ssh 
文件id_rsa表示私钥 id_rsa.pub表示公钥

6.设置git账户用户名和邮箱
git config user.email "xizhao.yh@gmail.com"
git config user.name "xizhao"

7.本地git库与github创建连接
git remote add origin git@github.com:xizhao-yh/yTile.git


8.本地文件删除以后如何再次下载
git checkout ./
git reset HEAD 回退到未提交操作
git mv main.cpp Src/ 移动文件