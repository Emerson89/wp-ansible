# -*- mode: ruby -*-
# vi: set ft=ruby :

vms = {
'almalinux-srv' => {'memory' => '1024', 'cpus' => '1', 'ip' => '11', 'box' => 'almalinux/8'},
'centos-srv' => {'memory' => '1024', 'cpus' => '1', 'ip' => '12', 'box' => 'centos/7'},
#'almalinux-srv' => {'memory' => '1024', 'cpus' => '1', 'ip' => '12', 'box' => 'almalinux/8'},
}

Vagrant.require_version '>= 2.0.0'

Vagrant.configure('2') do |config|
  vms.each do |name, conf|
     config.vm.define "#{name}" do |my|
       my.vm.box = conf['box']
       my.vm.hostname = "#{name}.example.com"
       #my.vm.network 'private_network', ip: "192.168.33.#{conf['ip']}"
       my.vm.network 'private_network', ip: "172.16.0.#{conf['ip']}"
       my.vm.provision "ansible" do |ansible|
          ansible.playbook = "playbook.yml"
       end
       my.vm.provider 'virtualbox' do |vb|
          vb.memory = conf['memory']
          vb.cpus = conf['cpus']
       end
     end
  end
end
