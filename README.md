# k8s-vagrant

1 Master dan 1 node




Tahapan instalasi kubernetes dengan vagrant :

1. install plugin untuk resize disk karena defaultnya hanya 10 GB disini kita ubah jadi 40GB, berikut command install plugin
   - vagrant plugin install vagrant-disksize
   
2. jalankan vagrant
   - vagrant up   



Note : jika ingin tambahkan node, ditambahnkan command berikut :
<code>{ /
        :name => "k8s-node-2", /
        :type => "node", /
        :box => "ubuntu/bionicl64", /
        :box_version => "20190716.0.0", /
        :eth1 => "192.168.205.12", /
        :mem => "2048", /
        :cpu => "2" /
       } /
</code>
