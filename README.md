# -SSH-
实现SSH免密跳转
ØpenSSH是SSH协议的免费开源实现，由客户端和f服务端的软件组成ss

生成公钥 
ssh-keygen -t rsa         
ssh-keygen -t  rsa
Generating public/private rsa key pair.
Enter file in which to save the key (/root/.ssh/id_rsa): 
/root/.ssh/id_rsa already exists.
Overwrite (y/n)? y
Enter passphrase (empty for no passphrase): 
Enter same passphrase again: 
Your identification has been saved in /root/.ssh/id_rsa.
Your public key has been saved in /root/.ssh/id_rsa.pub.
The key fingerprint is:
SHA256:o2TP9sFDGIrHCD1FqaI9P1yBpwSgQ3JtBvtUBtxUucg root@服务端
The key's randomart image is:
+---[RSA 2048]----+
|ooo+.=*o..       |
|+..o=+o .        |
|o o+++ ...       |
| ..++=E..o       |
| o o+o*.S .      |

2。将公钥拷贝给客户端并c重命名为 authorized_keys   
root@客户端 ~]# cd .ssh/
[root@客户端 .ssh]# ll
total 16
-rw-------. 1 root root 1200 Dec 27 17:06 authorized_keys
-rw-------. 1 root root 1675 Dec 27 16:53 id_rsa
-rw-r--r--. 1 root root  396 Dec 27 16:53 id_rsa.pub
-rw-r--r--. 1 root root  177 Dec 27 16:52 known_hosts
[root@服务端 ~]# ssh  root@169.254.134.129
Last failed login: Fri Dec 27 17:06:04 CST 2019 from 169.254.134.128 on ssh:notty
There was 1 failed login attempt since the last successful login.
Last login: Fri Dec 27 16:52:58 2019 from 客户端
               
下载上传
yum -y install lrzsz
下载sz
上传rz

