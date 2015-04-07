$prepare = <<SCRIPT
sudo apt-get update
sudo apt-get -qqy install redis-server
SCRIPT

Vagrant.configure(2) do |config|
  config.vm.box = "ubuntu/trusty64"
  config.vm.define "ansible-ruby-compiled" do |x|
  end
  config.vm.provision "shell", inline: $prepare
  config.vm.provision "shell",
    :path => "tests/specs.sh",
    :upload_path => "/home/vagrant/specs",
    # change role name below
    :args => "--install ansible-ruby-compiled"
end
