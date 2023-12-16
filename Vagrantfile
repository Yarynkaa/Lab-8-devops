Vagrant.configure("2") do |config|

  config.vm.box = "centos/7"

  config.vm.network "forwarded_port", guest: 80, host: 8888, host_ip: "127.0.0.1"
  config.vm.network "forwarded_port", guest: 443, host: 8443, host_ip: "127.0.0.1"

  config.vm.provision "shell", path: "script.sh"

  config.vm.synced_folder "content/", "/home/vagrant/shared/", type: "rsync"
end
