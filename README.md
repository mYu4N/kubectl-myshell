# kubectl-myshell
use kubectl myshell run a pod use root shell on k8s-node 

download the file into /usr/local/bin/kubectl-myshell

chmod 755 /usr/local/bin/kubectl-myshell

kubectl myshell node-name

[root@iZ2ze***3uhsZ my-bpftrace]# kubectl get nodes
NAME                        STATUS   ROLES    AGE    VERSION
cn-beijing.192.168.0.17     Ready    <none>   173d   v1.18.8-aliyun.1
cn-beijing.192.168.0.246    Ready    <none>   611d   v1.18.8-aliyun.1
cn-beijing.192.168.66.175   Ready    <none>   416d   v1.18.8-aliyun.1
cn-beijing.192.168.88.154   Ready    <none>   528d   v1.18.8-aliyun.1
cn-beijing.192.168.88.156   Ready    <none>   393d   v1.18.8-aliyun.1
cn-beijing.192.168.88.23    Ready    <none>   30d    v1.18.8-aliyun.1
[root@iZ2z****uhsZ my-bpftrace]# kubectl myshell cn-beijing.192.168.88.23
spawning "nsenter-7wmuc4" on "cn-beijing.192.168.88.23"

If you don't see a command prompt, try pressing enter.

[root@iZ2ze****1cpZ /]# 
[root@iZ2z****cpZ /]# ifconfig
cilium_host: flags=4291<UP,BROADCAST,RUNNING,NOARP,MULTICAST>  mtu 1500
        inet 169.254.10.2  netmask 255.255.255.255  broadcast 0.0.0.0
        inet6 fe80::2425:ff:feeb:8c44  prefixlen 64  scopeid 0x20<link>
        inet6 fc00::10ca:1  prefixlen 128  scopeid 0x0<global>
        ether 26:25:00:eb:8c:44  txqueuelen 1000  (Ethernet)
        RX packets 8  bytes 799 (799.0 B)
        RX errors 0  dropped 0  overruns 0  frame 0
        TX packets 13  bytes 1196 (1.1 KiB)
        TX errors 0  dropped 0 overruns 0  carrier 0  collisions 0
