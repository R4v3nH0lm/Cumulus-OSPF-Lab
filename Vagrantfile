Vagrant.configure("2") do |config|
  
  config.vm.define "web1" do |web1|
    web1.vm.hostname = "web1"
    web1.vm.box = "ubuntu/xenial64"
    web1.vm.provider :virtualbox do |vb|
      vb.customize ["modifyvm", :id, "--memory", "512"]
      vb.customize ["modifyvm", :id, "--cpus", "1"]
      vb.customize ["modifyvm", :id, "--cpuexecutioncap", "50"]
    end
    web1.vm.network "private_network", virtualbox__intnet: "swp1", ip: "10.10.10.2"
    # web1.vm.network "private_network", virtualbox__intnet: "swp2"
    # web1.vm.network "private_network", virtualbox__intnet: "swp3"
    # web1.vm.network "private_network", virtualbox__intnet: "swp4"
    # web1.vm.provision "shell", path: "nginx_install.sh"
  end

  config.vm.define "leaf1" do |leaf1|
    leaf1.vm.hostname = "leaf1"
    leaf1.vm.box = "CumulusCommunity/cumulus-vx"
    leaf1.vm.box_version = "3.1.2"
    leaf1.vm.provider :virtualbox do |vb|
      vb.customize ["modifyvm", :id, "--memory", "512"]
      vb.customize ["modifyvm", :id, "--cpus", "1"]
      vb.customize ["modifyvm", :id, "--cpuexecutioncap", "50"]
    end
    leaf1.vm.network "private_network", virtualbox__intnet: "swp1"
    leaf1.vm.network "private_network", virtualbox__intnet: "swp2"
    # leaf1.vm.network "private_network", virtualbox__intnet: "swp3"
    # leaf1.vm.network "private_network", virtualbox__intnet: "swp4"
  end

  config.vm.define "spine1" do |spine1|
    spine1.vm.hostname = "spine1"
    spine1.vm.box = "vEOS-lab-4.17.3F"
    # spine1.vm.network "private_network", virtualbox__intnet: "swp1"
    spine1.vm.network "private_network", virtualbox__intnet: "swp2"
    spine1.vm.network "private_network", virtualbox__intnet: "swp3"
    # spine1.vm.network "private_network", virtualbox__intnet: "swp4"
  end

  config.vm.define "leaf2" do |leaf2|
    leaf2.vm.hostname = "leaf2"
    leaf2.vm.box = "CumulusCommunity/cumulus-vx"
    leaf2.vm.box_version = "3.1.2"
    leaf2.vm.provider :virtualbox do |vb|
      vb.customize ["modifyvm", :id, "--memory", "512"]
      vb.customize ["modifyvm", :id, "--cpus", "1"]
      vb.customize ["modifyvm", :id, "--cpuexecutioncap", "50"]
    end
    # leaf2.vm.network "private_network", virtualbox__intnet: "swp1"
    # leaf2.vm.network "private_network", virtualbox__intnet: "swp2"
    leaf2.vm.network "private_network", virtualbox__intnet: "swp3"
    leaf2.vm.network "private_network", virtualbox__intnet: "swp4"
  end

  config.vm.define "web2" do |web2|
    web2.vm.hostname = "web2"
    web2.vm.box = "ubuntu/xenial64"
    web2.vm.provider :virtualbox do |vb|
      vb.customize ["modifyvm", :id, "--memory", "512"]
      vb.customize ["modifyvm", :id, "--cpus", "1"]
      vb.customize ["modifyvm", :id, "--cpuexecutioncap", "50"]
    end
    # web2.vm.network "private_network", virtualbox__intnet: "swp1"
    # web2.vm.network "private_network", virtualbox__intnet: "swp2"
    # web2.vm.network "private_network", virtualbox__intnet: "swp3"
    web2.vm.network "private_network", virtualbox__intnet: "swp4", ip: "10.30.30.2"
    # web2.vm.provision "shell", path: "nginx_install.sh"
  end

end