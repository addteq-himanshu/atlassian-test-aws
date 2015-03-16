Vagrant.configure(2) do |config|
  config.vm.box = 'chef/centos-6.6'

  config.omnibus.chef_version = :latest

  config.vm.network 'private_network', ip: '192.168.33.10'
  config.vm.provider 'virtualbox' do |vb|
    vb.memory = '1024'
  end

  config.vm.provision 'chef_solo' do |chef|
    chef.add_recipe 'jira'
    chef.add_recipe 'stash'
    chef.add_recipe 'bamboo'
  end
end