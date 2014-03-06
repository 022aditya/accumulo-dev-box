# Introduction

Spins up a VM with the Cloudera builds of Hadoop and Zookeeper (cdh3u3, as per my project requirements),
and Accumulo 1.4.3.

# Getting Started

1. [Download and install VirtualBox](https://www.virtualbox.org/wiki/Downloads)
2. [Download and install Vagrant 1.2.2](http://downloads.vagrantup.com/tags/v1.2.2)
3. Run ```vagrant box add precise64 http://files.vagrantup.com/precise64.box```
4. Clone this project
5. Run ```vagrant up``` from within the project directory. You'll need at least 2Gb free.
6. Run ```vagrant ssh``` from within the project directory to get into your VM, or open up the VirtualBox
   Manager app to tweak settings, forward ports, etc.
7. The app can now be accessed at port 10.211.55.100. To make it accessible at "accumulo-dev-box", add
   the following to the end of your /etc/hosts file: ```10.211.55.100 accumulo-dev-box```. (This step is already done     if you executed do_as_root_user.sh)


# Connecting to VM using PuTTY:
1. Open VirtualBox. Go to Settings for this VM. [If you're already running the VM, please shut it down first.]
2. In the Settings tab, select Network. Click on Advanced button on the right, and then click on Port Forwarding.
3. Add the following rule:<br />
   ```Protocol = TCP, Host IP = , Host Port = 2222, Guest IP = , Guest Port = 22```<br/>
   Note: No need to specify anything for Host IP and Guest IP, it's okay to leave them blank!
4. Save everything.
5. Boot up the VM.
6. Open PuTTY.
7. Specify<br />
   Host Name: ```127.0.0.1```<br />
   Port: ```2222```<br />
   Click Open.
8. Once the terminal opens and prompts you for credentials, enter:<br />
   Username: ```vagrant``` <br />
   Password: ```vagrant```
