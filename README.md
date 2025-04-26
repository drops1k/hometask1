Hometask 1
This repository contains the solution for the hometask 1 assignment. The goal of this assignment was to create a Vagrant environment with a CentOS 7 virtual machine provisioned with Nginx server. The Nginx server is configured to serve content placed in the ~/www-content directory on port 8888.

Requirements
Vagrant
VirtualBox (or another supported virtualization provider)
Usage
Clone this repository to your local machine
Change into the cloned directory
Start the Vagrant environment
Once the Vagrant environment is up and running, you can access the Nginx server by opening a web browser and navigating to http://localhost:8888.
Stop the Vagrant environment
Project Structure
Vagrantfile: Contains the configuration for the Vagrant environment, including the provisioning of the CentOS 7 virtual machine and Nginx server setup.
www-content/: Directory where you can place the content you want to be served by the Nginx server.
