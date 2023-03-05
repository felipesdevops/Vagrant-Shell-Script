Vagrant.configure("2") do |config|
  
  #Configurando ISO de SO com vm.box
  config.vm.box = "bento/ubuntu-20.04"
  config.vm.network "public_network", ip: "192.168.0.70", bridge: "eth1"
  config.vm.hostname = "ubuntu20-shell"
  #Configurando CPU e Memória da VM com vm.provider 
  config.vm.provider "virtualbox" do |v|
  v.memory = 1024
  v.cpus = 1
  end
  
  #Instalando aplicações por script
  config.vm.provision "shell",
	path: "script.sh"
	
  # Instalar aplicações no momento do provisionamento da vm com inline
  #config.vm.provision "shell",
   # inline: "apt update && apt install -y nginx && service nginx start"
  #fim

end
