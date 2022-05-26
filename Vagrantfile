Vagrant.configure("2") do |config|
	#set box to Bionic Beaver Ubuntu
	config.vm.box = "hashicorp/bionic64"
	#Use a private network
	config.vm.network "private_network", ip: "192.168.50.2"
	#Copy vim config, git config, vim plugins, and ssh key
	#config.vm.provision "file", source: "global_resources/gitconfig", destination: "~/.gitconfig"
	#config.vm.provision "file", source: "global_resources/vimrc", destination: "~/.vimrc"
	#config.vm.provision "file", source: "global_resources/plug.vim", destination: "~/.vim/autoload/plug.vim"
	#config.vm.provision "file", source: "global_resources/sshkey", destination: "~/.ssh/id-ed25519"
	#config.vm.provision "file", source: "global_resources/sshpub", destination: "~/.ssh/id_ed25519.pub"
	#Install vim plugins and update everything
	#config.vm.provision "shell", inline: <<-SHELL
		vim -c ":PlugInstall" -c ":qa!"
		apt-get -y update
		apt-get -y upgrade
	SHELL
	config.vm.provider "virtualbox" do |vb|
		vb.cpus = 2 #Ubuntu requires at least 2 CPUs
	end
end
