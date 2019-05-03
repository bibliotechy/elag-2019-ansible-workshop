# All Vagrant configuration is done below. The "2" in Vagrant.configure
# configures the configuration version (we support older styles for
# backwards compatibility). Please don't change it unless you know what
# you're doing.
Vagrant.configure(2) do |config|
  config.vm.provider "virtualbox" do |v|
    v.memory = 2048
    v.cpus = 1
  end
  config.vm.box = 'centos/7'

  config.vm.network 'forwarded_port', guest: 9200, host: 9200
  
  config.vm.provision 'ansible' do |ansible|
      ansible.playbook = 'playbook.yml'
      ansible.host_key_checking = false
      ansible.inventory_path = 'inventory/vagrant/'
      ansible.limit = 'all'
    end
  end
