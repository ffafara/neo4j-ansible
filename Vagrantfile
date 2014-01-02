VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = 'precise64'
  config.vm.hostname = 'neo4j-dev'
  config.vm.network "private_network", ip: "192.168.22.33"

  config.vm.provider "vmware_fusion" do |v, override|
    override.vm.box = "raring64_fusion"
    config.vm.box_url = 'https://s3.amazonaws.com/life360-vagrant/raring64.box'
  end
  config.vm.provision "ansible" do |ansible|
    ansible.playbook = "ansible/main.yml"
  end
  
end