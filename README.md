# Development environment for the Kopano WebApp Theming Workshop 2017
This guide will help you set up your development environment for the Theming Workshop at the Kopano Conference 2017.

## VirtualBox
Make sure you have VirtualBox installed. If you haven't please download the version you need from https://www.virtualbox.org/wiki/Downloads

## Virtual Machine
You can download the virtual machine (VM) that we will use for the workshop at https://owncloud.kopano.com/index.php/s/SjbqnXNnlo6YNj0
Download it and "import" it in VirtualBox. After that you should be able to "start" the VM. It contains a debian 8 setup with Kopano Core and Kopano WebApp installed.

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

## Editing files
The files of the WebApp can be found in the VM at /usr/share/kopano-webapp. The editors nano and vim have been installed in the VM, so those can be used to edit files directly. 

However, if you are like me and want to use your own editor, you can create a "Shared Folder" in VirtualBox. To do this you should close the VM and open its settings in VirtualBox. On the tab "Shared Folder" you can add a folder by clicking on the icon with the +. In the dialog that pops up you can chose a "Folder Path" on your laptop that you will share. Make sure that for "Folder Name" you will fill in "theming2017". Now start up your VM and check that the folder /media/sf_theming2017 exists. Copy the WebApp files to this directory:
```
cp -r /usr/share/kopano-webapp /media/sf_theming2017
```
The files are now copied to the shared folder on your laptop where you can edit them with any editor that you have installed. You can open this version of the WebApp in your browser by typing the following address in the address bar:
http://192.168.56.101/shared-kopano-webapp
