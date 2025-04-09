Vagrant.configure("2") do |config|
    config.vm.box = "Ubuntu/focal64"
  
    (1..2).each do |i|
      config.vm.define "web#{i}" do |web|
        web.vm.hostname = "web#{i}"
        web.vm.network "private_network", ip: "192.168.56.10#{i}"  # Changed from 192.168.1.10#{i}
      end
    end
  
    config.vm.define "db01" do |db|
      db.vm.hostname = "db01"
      db.vm.network "private_network", ip: "192.168.56.103"  # Changed from 192.168.1.103
    end
  
    config.vm.define "monitor01" do |monitor|
      monitor.vm.hostname = "monitor01"
      monitor.vm.network "private_network", ip: "192.168.56.104"  # Changed from 192.168.1.104
    end
  end