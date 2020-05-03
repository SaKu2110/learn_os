# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|
	config.vm.define "ubuntu" do |node|
		node.vm.box = "ubuntu/bionic64"
		node.vm.hostname = "saku2110"

		node.vm.provision "file", source: "./work", destination: "$HOME/work"

		node.vm.provision "shell", inline: <<-SHELL
		apt update
		apt upgrade
		apt install -y make sysstat build-essential
		SHELL
	end
end