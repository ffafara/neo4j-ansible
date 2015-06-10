VAGRANTFILE_API_VERSION = '2'

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = 'hashicorp/precise64'
  config.vm.hostname = 'neo4j-dev'
  config.vm.network "forwarded_port", guest: 7474, host: 7474
  config.vm.network 'private_network', ip: "192.168.33.10"

  config.vm.provision 'ansible' do |ansible|
    ansible.playbook = 'ansible/main.yml'
    ansible.inventory_path = 'Inventory'
    ansible.limit = 'all'
  end
end
