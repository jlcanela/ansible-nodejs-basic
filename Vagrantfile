VAGRANTFILE_API_VERSION = "2"
Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  # Use the same key for each machine
  config.ssh.insert_key = false
  config.vm.define "vagrant1" do |vagrant1|
    vagrant1.vm.box = "ubuntu/trusty64"
    vagrant1.vm.network "private_network", type: "dhcp"
  end
  config.vm.define "vagrant2" do |vagrant2|
     vagrant2.vm.box = "ubuntu/trusty64"
     vagrant2.vm.network "private_network", type: "dhcp"
   end
   config.vm.define "vagrant3" do |vagrant3|
     vagrant3.vm.box = "ubuntu/trusty64"
     vagrant3.vm.network "forwarded_port", guest: 80, host: 8080
     vagrant3.vm.network "private_network", type: "dhcp"
   end
end
