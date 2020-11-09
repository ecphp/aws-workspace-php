Vagrant.configure("2") do |config|
    config.vm.box = "bento/amazonlinux-2"

    config.vm.provider "virtualbox" do |vb|
        vb.memory = "2048"
    end

    config.vm.provision "ansible" do |ansible|
        ansible.playbook = "site.yml"
        ansible.limit = "all"
    end
end
