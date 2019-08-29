# k8s-vagrant 
# Kubernetes cluster terdiri 1 Master dan 1 node worker

spesifikasi :
- ubuntu bionic64
- docker 18.09

----------------------------------------------------------------------------------------------------------------------------

Tahapan instalasi kubernetes dengan vagrant :
1. Install [Virtualbox versi 6.0](https://www.virtualbox.org/wiki/Downloads)

2. Install [Vagrant](https://www.vagrantup.com/downloads.html)

3. install plugin untuk resize disk karena defaultnya hanya 10 GB disini kita ubah jadi 40GB, berikut command install plugin
```
vagrant plugin install vagrant-disksize
```
   
4. copy vagrantfile ke folder tujuan, buka cmd dan masuk ke directory tujuan tadi kemudian jalankan vagrant
```
vagrant up   
```


Note : jika ingin tambahkan node, ditambahnkan command berikut :
```
{ 
   :name => "k8s-node-2", 
   :type => "node", 
   :box => "ubuntu/bionicl64", 
   :box_version => "20190716.0.0", 
   :eth1 => "192.168.205.12", 
   :mem => "2048", 
   :cpu => "2" 
} 
```

untuk menghapus cluster
```
vagrant destroy -f
```

untuk mematikan dan ingin menghidupkan kembali suatu saat

matikan :
```
vagrant halt
```
Hidupkan:
```
vagrant reload
```


credits
```
https://github.com/ecomm-integration-ballerina/kubernetes-cluster.git
```
