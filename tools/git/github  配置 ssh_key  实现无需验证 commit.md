# 文章目录
1. 设置 git 的 user name email
2. 检查 git 应用是否存在 SSH_Key
3. 获取 SSH_Key
4. GitHub 添加 SSH_Key
5. 验证和修改


### 一、设置 git 的 name password email
```
git config --global user.name diankenan
git config --global user.password who1154761092
git config --global user.email 2687752099@qq.com
```
### 二、检查是否存在 SSH Key


```
cd ~/.ssh
ll //看是否存在 id_rsa 和 id_rsa.pub 文件，如果存在，说明已经有 SSH Key

Administrator@DESKTOP-KQC9JJL MINGW64 ~
$ cd ~/.ssh
Administrator@DESKTOP-KQC9JJL MINGW64 ~/.ssh
$ ls
id_rsa  id_rsa.pub

```

###### 如果没有 SSH Key，则需要先生成一下
```
ssh-keygen -t rsa -C "2687752099@qq.com"

```

### 三、获取SSH Key
```
cat id_rsa.pub
//拷贝秘钥 ssh-rsa开头
ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDHCKLeHTjXOFWPhstJtRa/Lwo5A+a+Y3W7WtIc2ATf    
2W3WWE4EERR0YFTz6Zy1fQENPfxC1ZD2VKAxIZ5XZ93ufQJZKry1JnrWxL0XSao3K+b7cQpZTW1aXxcm       
+lJAiaMbrQ4g5SsyfispfmB9fw3gm5qRegTY4aJhly5vBJNkwSc5AmEQQ3yZIMDxeXII+6tDhJv1rSaB       
ow6z/FlzxHB/rkE0FMKc/1VX4J2GzPAHFHALVImkF/JPvNV/a5h8MblwBOWqyPoYsIwBSpbGhYDjYBVD       
rh5CFKGf8HT6DF5f9blV6nKcMV6MAhLz0fARBblVeGIeS2nb/pJMhzLnrFJD Administrator@DESKT       
OP-KQC9JJL
```
### 四、GitHub添加SSH Key

- GitHub点击用户头像，选择setting
- SSH and GPG keys
- new SSH Key
- 取个名字，把之前拷贝的秘钥复制进去，添加就好啦。
- add SSH Key

### 五、验证和修改

```
ssh -T git@github.com
//运行结果出现类似如下
Hi xiangshuo1992! You've successfully authenticated, but GitHub does not provide shell access.
```
