Vagrant.configure("2") do |config|
    config.vm.box = "generic/centos9s"
    config.vm.network "forwarded_port", guest: 80, host: 8888
    
    # Create a shared folder for www content
    config.vm.synced_folder "./www-content", "/var/www/html", create: true
    
    config.vm.provision "shell", inline: <<-SHELL
      yum install -y epel-release
      yum install -y nginx
      setenforce 0
      sed -ie 's/^SELINUX=.*$/SELINUX=disabled/' /etc/selinux/config
      cat /etc/selinux/config
      systemctl start nginx
      systemctl enable nginx
      systemctl disable firewalld
      systemctl stop firewalld
    SHELL
  end