Vagrant.configure("2") do |config|

  config.vm.define "master" do |master|
    master.vm.box = "generic/centos8"
    master.vm.network "public_network" , ip: "172.23.89.10"
    master.vm.synced_folder ".", "/vagrant", disabled: false
    master.vm.provider "virtualbox" do |vb|
     vb.memory = "4096"
   end
   master.vm.provision "shell", inline: <<-SHELL
     echo "nameserver 8.8.8.8" >> /etc/resolv.conf
     sudo sed -i 's/mirrorlist/#mirrorlist/g' /etc/yum.repos.d/CentOS-* && sed -i 's|#baseurl=http://mirror.centos.org|baseurl=http://vault.centos.org|g' /etc/yum.repos.d/CentOS-*
     sudo dnf install epel-release python39 git-core -y
     sudo dnf install python39-PyYAML python39-cryptography python39-six -y
     wget http://mirror.centos.org/centos/8-stream/AppStream/x86_64/os/Packages/ansible-core-2.13.3-1.el8.x86_64.rpm
     wget http://mirror.centos.org/centos/8-stream/AppStream/x86_64/os/Packages/sshpass-1.09-4.el8.x86_64.rpm
     sudo rpm -ivh sshpass-1.09-4.el8.x86_64.rpm ansible-core-2.13.3-1.el8.x86_64.rpm
     sudo mv /vagrant/sshd_config /etc/ssh/
     sudo systemctl restart sshd
   SHELL
  end
  
    config.vm.define "srv1" do |srv1|
    srv1.vm.box = "generic/centos8"
    srv1.vm.network "public_network" , ip: "172.23.89.11"
    srv1.vm.synced_folder ".", "/vagrant", disabled: false
    srv1.vm.provider "virtualbox" do |vb|
     vb.memory = "2048"
   end
   srv1.vm.provision "shell", inline: <<-SHELL
     echo "nameserver 8.8.8.8" >> /etc/resolv.conf
     sudo sed -i 's/mirrorlist/#mirrorlist/g' /etc/yum.repos.d/CentOS-* && sed -i 's|#baseurl=http://mirror.centos.org|baseurl=http://vault.centos.org|g' /etc/yum.repos.d/CentOS-*
     sudo dnf install epel-release python39 git-core -y
     sudo dnf install python39-PyYAML python39-cryptography python39-six -y
     wget http://mirror.centos.org/centos/8-stream/AppStream/x86_64/os/Packages/ansible-core-2.13.3-1.el8.x86_64.rpm
     wget http://mirror.centos.org/centos/8-stream/AppStream/x86_64/os/Packages/sshpass-1.09-4.el8.x86_64.rpm
     sudo rpm -ivh sshpass-1.09-4.el8.x86_64.rpm ansible-core-2.13.3-1.el8.x86_64.rpm
     sudo mv /vagrant/sshd_config /etc/ssh/
     sudo systemctl restart sshd
   SHELL
  end
  
    config.vm.define "srv2" do |srv2|
    srv2.vm.box = "generic/centos8"
    srv2.vm.network "public_network" , ip: "172.23.89.12"
    srv2.vm.synced_folder ".", "/vagrant", disabled: false
    srv2.vm.provider "virtualbox" do |vb|
     vb.memory = "2048"
   end
   srv2.vm.provision "shell", inline: <<-SHELL
     echo "nameserver 8.8.8.8" >> /etc/resolv.conf
     sudo sed -i 's/mirrorlist/#mirrorlist/g' /etc/yum.repos.d/CentOS-* && sed -i 's|#baseurl=http://mirror.centos.org|baseurl=http://vault.centos.org|g' /etc/yum.repos.d/CentOS-*
     sudo dnf install epel-release python39 git-core -y
     sudo dnf install python39-PyYAML python39-cryptography python39-six -y
     wget http://mirror.centos.org/centos/8-stream/AppStream/x86_64/os/Packages/ansible-core-2.13.3-1.el8.x86_64.rpm
     wget http://mirror.centos.org/centos/8-stream/AppStream/x86_64/os/Packages/sshpass-1.09-4.el8.x86_64.rpm
     sudo rpm -ivh sshpass-1.09-4.el8.x86_64.rpm ansible-core-2.13.3-1.el8.x86_64.rpm
     sudo mv /vagrant/sshd_config /etc/ssh/
     sudo systemctl restart sshd
   SHELL
  end
  
    config.vm.define "srv3" do |srv3|
    srv3.vm.box = "generic/centos8"
    srv3.vm.network "public_network", ip: "172.23.89.13"
    srv3.vm.synced_folder ".", "/vagrant", disabled: false
    srv3.vm.provider "virtualbox" do |vb|
     vb.memory = "2048"
   end
   srv3.vm.provision "shell", inline: <<-SHELL
     echo "nameserver 8.8.8.8" >> /etc/resolv.conf
     sudo sed -i 's/mirrorlist/#mirrorlist/g' /etc/yum.repos.d/CentOS-* && sed -i 's|#baseurl=http://mirror.centos.org|baseurl=http://vault.centos.org|g' /etc/yum.repos.d/CentOS-*
     sudo dnf install epel-release python39 git-core -y
     sudo dnf install python39-PyYAML python39-cryptography python39-six -y
     wget http://mirror.centos.org/centos/8-stream/AppStream/x86_64/os/Packages/ansible-core-2.13.3-1.el8.x86_64.rpm
     wget http://mirror.centos.org/centos/8-stream/AppStream/x86_64/os/Packages/sshpass-1.09-4.el8.x86_64.rpm
     sudo rpm -ivh sshpass-1.09-4.el8.x86_64.rpm ansible-core-2.13.3-1.el8.x86_64.rpm
     sudo cp /vagrant/sshd_config /etc/ssh/
     sudo systemctl restart sshd
   SHELL
  end
  
end