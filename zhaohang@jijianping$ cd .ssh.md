> zhaohang@jijianping:~$ cd .ssh
> zhaohang@jijianping:~/.ssh$ ls
> authorized_keys  id_rsa  id_rsa.pub  known_hosts
> zhaohang@jijianping:~/.ssh$ vim authorized_keys
> zhaohang@jijianping:~/.ssh$ sudo -i
> [sudo] zhaohang 的密码： 
> root@jijianping:~# cd .ssh
> -bash: cd: .ssh: 没有那个文件或目录
> root@jijianping:~# ^C
> root@jijianping:~# 注销
> zhaohang@jijianping:~/.ssh$ vim authorized_keys 
> zhaohang@jijianping:~/.ssh$ cd
> zhaohang@jijianping:~$ cp -r ~zhaohang/.ssh/ ~root
> cp: 无法获取'/root/.ssh' 的文件状态(stat): 权限不够
> zhaohang@jijianping:~$ sudo !!
> sudo cp -r ~zhaohang/.ssh/ ~root
> zhaohang@jijianping:~$ sudo -i
> root@jijianping:~# cd .ssh
> root@jijianping:~/.ssh# ls
> authorized_keys  id_rsa  id_rsa.pub  known_hosts
> root@jijianping:~/.ssh# cat authorized_keys 
> ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAABAQDHJY+HkBWMinw48xW4ZKDrdkNQ8332lZSRPfbgWtntcDtKvzknTsNLO24P+pinFlF3O1Sd9YnQrWZG/JVp5ybjW00qXeAu4JVnBjZ39/Ws9/pd/FAjUQigQDv2oFb/jMGvBiEvQS2e1YwH0o4o3aigGavZcmCCme6kJLTPHFeZpLyBd6vmBn2NdmS6Jx9shaHg6mU7ZYpVzmQ2kpEQzcIzDRGlqcIwL9UNXMOmRhR0UqoC9kz29zRf06W+Fp9l4xJHInoKqhGxL5Hb9mVma2LTy4XTzyMsgznrSHuQ5jkn4z9pNHuRg4+3LNjuM/9D547lVnp9czVxx59KlSFxcbdF zhaohang@pi19
> ssh-rsa AAAAB3NzaC1yc2EAAAADAQABAAAAgQC2CLtRyEfOyMT7dQCm5XWzMGRqJLkMLfqkTr1fuwdB+7dhA4rLk8aQuURhFRa/ag2eTiyTdiVIaKcCaZglGJuMwI4cNiT4xMCy7uWbTBT4otjjqAxE5/tTdESIFkVs2DeTEi93uHHT7/MtswSQho+uyp5sM8CGWKccT+y5QCO9NQ== suyelu@bogon
> root@jijianping:~/.ssh# 
> root@jijianping:~/.ssh# 注销