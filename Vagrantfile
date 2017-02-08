Vagrant.configure("2") do |config|
  config.vm.box = "windows10"
  config.vm.guest = :windows

  # Configure Vagrant to use WinRM instead of SSH
  config.vm.communicator = "winrm"

  # Configure WinRM Connectivity
  config.winrm.username = "IEUser"
  config.winrm.password = "Passw0rd!"

  config.vm.provider "virtualbox" do |vb|
     # Display the VirtualBox GUI when booting the machine
     vb.gui = true
   end

  # Run Ansible from the Vagrant Host
  # https://www.vagrantup.com/docs/provisioning/ansible.html
  # https://www.vagrantup.com/docs/provisioning/ansible_intro.html
  #config.vm.provision "ansible" do |ansible|
  #  ansible.playbook = "restexample-windows.yml"
  #  ansible.inventory_path = "hostsfile"
  #  ansible.limit = "restexample-windows-dev",
  #  ansible.extra_vars = {
  #    spring_boot_app_jar: "../restexamples/target/restexamples-0.0.1-SNAPSHOT.jar",
  #    spring_boot_app_name: "restexample-springboot",
  #    host: "restexample-windows-dev"
  #  }
  #end
end