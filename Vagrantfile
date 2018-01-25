Vagrant.configure(2) do |config|
  config.vm.provider "virtualbox" do |v|
    v.name = "blockchain-graveyard-jekyll"
  end

  config.vm.box = "ubuntu/trusty64"

  config.vm.network "forwarded_port", guest: 4000, host: 4000

  config.vm.provision "shell", privileged: false, inline: <<-SHELL
    echo "Provisioning Virtual Machine..."
    sudo apt-get update

    echo "Installing developer packages..."
    sudo apt-get install build-essential curl vim -y > /dev/null

    echo "Installing Git..."
    sudo apt-get install git -y > /dev/null


    echo "Installing RVM and Ruby..."
    gpg --keyserver hkp://keys.gnupg.net --recv-keys 409B6B1796C275462A1703113804BB82D39DC0E3
    gpg --list-keys D39DC0E3 > /dev/null
    if [[ $? != 0 ]]; then curl -sSL https://rvm.io/mpapis.asc | gpg --import - ; fi
    curl -sSL https://get.rvm.io | bash -s stable
    source /home/vagrant/.profile
    rvm install 2.2

    echo "Installing Jekyll..."
    gem install jekyll
    gem install bundler
  SHELL

  #config.vm.provision "shell", run: "always" do |s|
  #  s.inline = "/home/vagrant/.rvm/gems/ruby-2.2.7/bin/jekyll s -s /vagrant --host 0.0.0.0 --force_polling"
  #end

  config.vm.post_up_message = "Hi! To build the jekyll siteand run the server, login to the VM with \'vagrant ssh\' and then run \'jekyll serve -s /vagrant --host 0.0.0.0 --force_polling\'"

end
