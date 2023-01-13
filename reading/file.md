# 关于如何使用github进行更新和上传，以及配置



ssh-keygen.exe -o 生成一个本地电脑指定的密钥

```shell
$ ssh-keygen.exe -o
Generating public/private rsa key pair.
Enter file in which to save the key (/c/Users/熊/.ssh/id_rsa):
Enter passphrase (empty for no passphrase):
Enter same passphrase again:
Your identification has been saved in /c/Users/熊/.ssh/id_rsa
Your public key has been saved in /c/Users/熊/.ssh/id_rsa.pub
The key fingerprint is:
SHA256:hUts4jA9ENwWmwv2ZnbZlnXXh6buSRNyQz7OY8Rqij0 熊@DESKTOP-6DIF025
The key's randomart image is:
+---[RSA 3072]----+
|   .oo..         |
|    .oo+ .     ..|
|    =.* = . o + +|
|   . * * = * + ..|
|      B S = X    |
|     + . . O +   |
|          o O    |
|       oEo + +   |
|      . o.  o    |
+----[SHA256]-----+
```





去github设置中 shh 私人密钥，提交密钥，密钥文件就在 上一个命令输出的指定文件夹中

##  将存储库配置到本地



![image-20230113230515372](C:\Users\熊\AppData\Roaming\Typora\typora-user-images\image-20230113230515372.png)

找到对应库的 上面的ssh ，然后Git clone 一下，相当于下载，这个你可以到你想放的本地位置再使用该命令

```
git clone git@github.com:xiongsircool/xiongsircool.git
```

下载完成后直接就可以对里面数据进行修改等操作了，操作完成后就是对数据进行提交

```
git add .
git commit -m "add all"
git push
```



如果出现下面的报错就是要你配置下你的账号信息

```
$ git commit -m "add all"
Author identity unknown

*** Please tell me who you are.

Run

  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"

to set your account's default identity.
Omit --global to set the identity only in this repository.

fatal: unable to auto-detect email address (got '熊@DESKTOP-6DIF025.(none)')

```



那就是配置下邮箱和你的账户 ，只用该双引号内容就可以了，用户名就是点你头像应该可以找到

```
  git config --global user.email "you@example.com"
  git config --global user.name "Your Name"
```



