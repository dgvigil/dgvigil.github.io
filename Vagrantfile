# -*- mode: ruby -*-
# vi: set ft=ruby :

Vagrant.configure("2") do |config|

  config.vm.box = "ubuntu/xenial64"

  config.vm.network "forwarded_port", guest: 80, host: 8080

  config.vm.provider "virtualbox" do |vb|
    # Customize the amount of memory on the VM:
    vb.memory = "1024"
  end

  config.vm.synced_folder ".", "/srv/website", create: true

  #Installing Ruby/RVM
  config.vm.provision :shell, path: "dev/install-rvm.sh", args: "stable"
  config.vm.provision :shell, path: "dev/install-ruby.sh", args: "ruby-head"

  config.vm.provision "shell", inline: <<-SHELL
    cd /srv/website
    gem install bundler
    bundle install
    bundle exec jekyll serve --port 8080
  SHELL
end
