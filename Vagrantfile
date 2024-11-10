Vagrant.configure("2") do |config|
  # Configuración para DNSA (Maestro)

  config.vm.define "maestro" do |m|
    m.vm.box = "debian/bookworm64"
    m.vm.network "private_network", ip: "192.168.57.10"
    m.vm.hostname = "maestro"
    m.vm.provision "shell", inline: <<-SHELL
      apt-get update
      apt-get install -y bind9
    SHELL
  end

end