Vagrant.configure('2') do |config|
  config.vm.box = 'ubuntu/focal64'

  config.vm.provision 'ansible' do |ansible|
    ansible.playbook = 'playbook.yaml'
    ansible.compatibility_mode = '2.0'
    ansible.verbose = 'vv'
  end

  config.vm.define 'server' do |server|
    server.vm.hostname = 'server'
    server
  end

  config.vm.define 'client', primary: true do |client|
    client.vm.hostname = 'client'
  end
end
