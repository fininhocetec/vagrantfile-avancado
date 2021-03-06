# -*- mode: ruby -*-
# vi: set ft=ruby  :

machines = {
  "devops"      => {"memory" => "1536", "cpu" => "2", "ip" => "10", "image" => "centos/7"},
  "compliance"  => {"memory" => "1024", "cpu" => "2", "ip" => "20", "image" => "ubuntu/bionic64"},
  "docker"      => {"memory" => "1536", "cpu" => "1", "ip" => "30", "image" => "centos/7"},
  "git"          => {"memory" => "256",  "cpu" => "1", "ip" => "40", "image" => "debian/buster64"},
  "log"          => {"memory" => "2048", "cpu" => "1", "ip" => "50", "image" => "generic/ubuntu1804"}
}

Vagrant.configure("2") do |config|

  config.vm.box_check_update = false
  config.vm.boot_timeout = 600
  machines.each do |name, conf|
    config.vm.define "#{name}" do |machine|
      machine.vm.box = "#{conf["image"]}"
      machine.vm.hostname = "#{name}.example.local"
      machine.vm.network "private_network", ip: "10.10.0.#{conf["ip"]}"
      machine.vm.provider "virtualbox" do |vb|
        vb.name = "#{name}"
        vb.memory = conf["memory"]
        vb.cpus = conf["cpu"]
        vb.customize ["modifyvm", :id, "--groups", "/IaC"]
      end
    end
  end
  config.vm.provision "shell", path: "script.sh"
end