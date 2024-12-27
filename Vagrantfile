Vagrant.configure("2") do |config|
  config.vm.box = "ubuntu/bionic64"
  
  # VirtualBox-specific configurations
  config.vm.provider "virtualbox" do |vb|
    vb.gui = true
    vb.customize ["modifyvm", :id, "--uartmode1", "file", "C:\\vagrant-logs\\vm-console.log"]
  end

  # Disable shared folders if using WSL
  config.vm.synced_folder ".", "/vagrant", disabled: true
end

