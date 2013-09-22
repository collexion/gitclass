# vi: set ft=ruby :
VAGRANTFILE_API_VERSION = "2"

Vagrant.configure(VAGRANTFILE_API_VERSION) do |config|
  config.vm.box = "precise64"
  config.vm.box_url = "http://cloud-images.ubuntu.com/precise/current/" +
                      "precise-server-cloudimg-vagrant-amd64-disk1.box"
  config.ssh.forward_agent = true
  config.vm.synced_folder ".", "/home/vagrant/gitdata"

  config.vm.provision :shell do |shell|
    shell.inline = "apt-get update && apt-get install -y git vim nano"
  end
end
