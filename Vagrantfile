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
  config.vm.provision "ansible_local" do |ansible|
    ansible.playbook       = "playbook.yml"
    ansible.install_mode   = :pip
    ansible.inventory_path = "inventory/vagrant"
    ansible.limit          = "all"
    ansible.galaxy_role_file = "requirements.yml"
    ansible.galaxy_roles_path = "/etc/ansible/roles"
    ansible.galaxy_command = "sudo ansible-galaxy install --role-file=%{role_file} --roles-path=%{roles_path} --force"
  end


end
