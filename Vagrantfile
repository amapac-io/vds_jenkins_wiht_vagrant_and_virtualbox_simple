Vagrant.configure(2) do |config|
  config.vm.box = "bento/ubuntu-22.04" # <.>
  config.vm.network "forwarded_port", guest: 8080, host: 8080 # <.>
  config.vm.provider "virtualbox" do |vb|
    vb.name = "DevelopmentServer"
    vb.customize ["modifyvm", :id, "--cpus", "2"] # <.>
  end
  config.vm.provision "shell"  do |s|
    s.path = "bootstrap.sh" # <.>
  end
end
