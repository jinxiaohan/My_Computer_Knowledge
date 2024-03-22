一、检查本地主机是否已经存在ssh key
cd ~/.ssh
ls

二、生成ssh key
ssh-keygen -t rsa -C "xiaohanjin.private@outlook.com"

三、获取ssh key公钥内容（id_rsa.pub)
cd ~/.ssh
cat id_rsa.pub

四、添加公钥内容到GIT SETTINGS.SSH keys

五、验证是否设置成功
ssh -T git@github.com

man ssh-keygen // 查看帮助信息
example: ssh-keygen -t rsa -f ~/.ssh/id_rsa.github -C "xiaohanjin.private@outlook.com"
-t //  dsa | ecdsa | ed25519 | rsa Specifies the type of key to create. 指定生成key的类型
-f // filename：Specifies the filename of the key file. 指定保存文件名
-C // Provides a new comment. 提供新注释 "xiaohanjin.private@outlook.com"

确保有密码验证，以及私钥为:~/.ssh/id_rsa
