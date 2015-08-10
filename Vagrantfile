# -*- mode: ruby -*-
# vi: set ft=ruby :

dir = File.expand_path(File.dirname(__FILE__))
img = "lwieske.bmp"
#img = "vodafone.bmp"

Vagrant.configure(2) do |config|

  config.vm.box = "chef/centos-7.1"

  config.vm.provider "virtualbox" do |vb|
    vb.gui = true
    vb.memory = "1024"

    vb.customize ["modifyvm", :id,
      "--bioslogofadein",      "on",
      "--bioslogofadeout",     "on",
      "--bioslogodisplaytime", 5000,
      "--bioslogoimagepath",   dir + "/" + img,
      "--biosbootmenu",        "disabled"]
  end

end
