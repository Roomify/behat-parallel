Vagrant.configure("2") do |config|

  # Box
  config.vm.box = 'precise64'
  config.vm.box_url = 'http://files.vagrantup.com/precise64.box'

  # Shared folders
  config.vm.synced_folder '.', "/srv"

  # Setup
  config.vm.provision :shell, :inline => "apt-get update --fix-missing"
  config.vm.provision :shell, :inline => "apt-get install -q -y python-software-properties python g++ make git curl"
  config.vm.provision :shell, :inline => "add-apt-repository ppa:ondrej/php5 && apt-get update"
  config.vm.provision :shell, :inline => "apt-get install -q -y php5-cli php5-xdebug"
  config.vm.provision :shell, :inline => "curl -s https://getcomposer.org/installer | php"
  config.vm.provision :shell, :inline => "mv ./composer.phar /usr/local/bin/composer"

end
