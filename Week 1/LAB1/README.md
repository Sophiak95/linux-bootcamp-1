# Lab 1: Create a Linux virtual machine with the Azure CLI

1. Launch Azure Cloud Shell
2. Create a resource group
3. Create virtual machine
4. Open port 80 for web traffic
5. Connect to virtual machine
6. Install web server
7. View the web server in action

### Notes:

Quickstart: Create a Linux VM
* https://docs.microsoft.com/en-us/azure/virtual-machines/linux/quick-create-cli

Quickstart for Bash in Azure Cloud Shell
* https://docs.microsoft.com/en-us/azure/cloud-shell/quickstart

**LEARNINGS FROM COMPLETING LAB ONE**
**1. LAUNCHING AZURE CLOUD SHELL**
Azure cloud shell is an interactive, specially designed shell, that runs on the browser. It gives users access to the Azure Resource Manager, which can be used to configure all of the resources available on Azure Cloud.

It serves as an alternative to using the Azure console. You can choose if you would like to emulate either a Bash shell or a PowerShell while using the Azure Cloud Shell.

Using the cloud shell :-> Points noted.
To use the cloud shell, i had to subscribe to azuure. This means that it can also be classified as one of Azure's resources
To use the cloud shell you need to have a persistent disk. This volume retains data even after the power is turned off/ the container is destroyed.


**2. CREATING AN AZURE RESOURCE GROUP**
An azure resource group can be conceptualized as a folder which is used to group related, interdependent or logically linked Azure resources together.

When creating an Azure Resource Group,i specify the following:

The region you want the Resource Group to be located.
The name of the Resource Group that is being created.
You can also add various resources you want, to be part of the Resource Group created.

Please note that the reouseces present in a particular resource group should have a similar life cycle

**3. CREATING A VIRTUAL MACHINE**
An Azure Virtual Machine can be created using either the cloud shell or the Azure console. Which is the GUI we can see on the Azure Portal.

Using the Console, you can use the following steps to create the Virtual Machine.

Please note that this is also part of the subscription based plans on Azure, as you may be charged for creating Virtual Machines

Select the create Virtual Machine option from the console.
Specify the image you want the Virtual Machine to run on, this can also be seen as the operating system of the Virtual box.
Specify the port you want for inbound traffic
Create your Public and private Key Pairs whuch you would use to access and configure your Virtual box
Create your virtual box

**4. OPENING PORT 80 FOR WEB TRAFFIC.**
The virtual box comes with various ports which allow different kinds of connections.

Port 80 can be used for inbound traffic. This means that users on the internet can communicate with your compute instance via that port.

Port 22 can be used for ssh connections. This is to give remote access to your virtual box.

Kindly note that you can also specify the network protocols for each port. Usually by default, this is TCP

**5. CONNECTING TO THE VIRTUAL MACHINE**
SSH was used to connect to the virtual machine. This is like a Secure Shell.

The SSH protocol makes use of the key file, to connect you remotely to the virtual box environment. Once you are in you can perform other configurations on the machine, without baing on the Azure portal. You can do this locally via your local shell.

**6. INSTALLING A WEB SERVER ON THE VIRTUAL MACHINE**
The virtual machine does not come with a server installed. i installed a web on the platform, i ran the command: sudo apt-get -y install nginx

This installs the latest version of NGINX server on your VM.

**7. VIEWING THE WEBSERVER IN ACTION**
To do this, i went to my VM instance and click on the external IP address. It would redirect you to a URL which you would use to view your laund NGINX web page.
