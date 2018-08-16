# vagrant-centos-cluster

为了使用桥接网络模式（独立的 IP 地址访问），别忘了在Vagrantfile中，增加下面配置：
```
config.vm.network "public_network", bridge: "en0: Wi-Fi (AirPort)"
config.vm.boot_timeout = 2000
```
两个虚拟机创建好之后，使用下面命令，分别创建root账号：
```
$ vagrant ssh
$ sudo passwd root
$ su root
```
