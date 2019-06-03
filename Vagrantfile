Vagrant.configure(2) do |config|
  config.vm.box = "centos/7"

  config.vm.define :cyber do |cyber_config|
      cyber_config.vm.host_name = "cyber"
      cyber_config.vm.network "private_network", ip:"192.168.5.150"
      cyber_config.vm.network "private_network", ip:"192.168.7.150"
      cyber_config.vm.provider :virtualbox do |vb|
          vb.customize ["modifyvm", :id, "--memory", "512"]
          vb.customize ["modifyvm", :id, "--cpus", "2"]
      end
  end

  config.vm.define :dn01 do |dn01_config|
      dn01_config.vm.host_name = "dn01"
      dn01_config.vm.network "private_network", ip:"192.168.5.200"
      dn01_config.vm.provider :virtualbox do |vb|
          vb.customize ["modifyvm", :id, "--memory", "256"]
          vb.customize ["modifyvm", :id, "--cpus", "2"]
      end
  end
  config.vm.define :dn02 do |dn02_config|
      dn02_config.vm.host_name = "dn02"
      dn02_config.vm.network "private_network", ip:"192.168.5.201"
      dn02_config.vm.provider :virtualbox do |vb|
          vb.customize ["modifyvm", :id, "--memory", "256"]
          vb.customize ["modifyvm", :id, "--cpus", "2"]
      end
  end
end
												  
