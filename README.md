# Development environment for the Kopano WebApp Theming Workshop 2017
This guide will help you set up your development environment for the Theming Workshop at the Kopano Conference 2017.

## VirtualBox
Make sure you have VirtualBox installed. If you haven't please download the version you need from https://www.virtualbox.org/wiki/Downloads

## Virtual Machine
You can download the virtual machine (vm) that we will use for the workshop at https://owncloud.kopano.com/index.php/s/SjbqnXNnlo6YNj0
Download it and "import" it in VirtualBox. After that you should be able to "start" the vm. It contains a debian 8 setup with Kopano Core and Kopano WebApp installed.

You can log in as root with the password root.

Try to run
```
ip addr
```
to check if the network adapters have gotten an IP address.

Note: To use the "host-only" adapter VirtualBox should have a "host-only" network running with a dhcp server that hands out addresses. During the workshop we will assume your machine has the address 192.168.56.101. This is the default setting of VirtualBox, so if you have changed it you might need to change it back or use the address that VirtualBox gave to your adapter.

## Open the WebApp in a browser
To check if everything works you can open the WebApp in a browser by typing http://192.168.56.101/kopano-webapp in the address bar. You should see the login screen of the WebApp. Five users have been added to the system with the following credentials (username/password):
- user1/user1
- user2/user2
- user3/user3
- user4/user4
- user5/user5
