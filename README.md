# CMPE 283: Virtualization Technologies 
# Assignment 1: Discovering VMX Features
## Team Members: 
* Kiran Bala Devineni (SJSU ID: 015218866)
* Venkat Mannam (SJSU ID: 015263326)

## Q1. For each member in your team, provide 1 paragraph detailing what parts of the lab that member implemented / researched.

### Kiran Bala Devineni (SJSU ID: 015218866)

* Setup the environment in macOS using VMware Fusion and then installed Linux Ubuntu.

* Downloaded and built the Linux Kernel modules and associated libraries to create a local copy of Linux Kernel.

* Discussed and researched about MSRs to be read in the SDM.

* Modified the cmpe283-1.c code by adding the custom logic to enable our system to read and give output for capabilities of the various MSRs. 

* Contribution also includes MSR code for controls- Primary and Secondary Procbased controls, and discovering the VMX Features present in my processor (Intel) by               writing a Linux kernel module that queries these features.

* Tested and verified the proper working of the functionality of code by comparing it with the sample output given to us. 

* Simulating the answers for the questions in the README.md file.

### Venkat Mannam (SJSU ID: 015263326)

* Setup the environment in macOS using VMware Fusion and downloaded the Linux ISO file. 

* Built a VM successfully in the first attempt by allocating 150GB storage and 8GB RAM to it. 

* Tested the machine to check its capability for the VMX virtualization and feature recognition. 

* Researched and discussed about MSRs to be read in the SDM and contributed to writing and execution of the code.

* Contribution also includes MSR code for controls- Entry and Exit controls, and determining the availability of secondary procbased controls.

* Staged and committed the cmpe283-1.c code file and Makefile after inserting the module and printing out the buffer from the Kernel. 

* Generated a comprehensive diff file after committing the changes to the repository. 

## Q2. Describe in detail the steps you used to complete the assignment. 

This assignment focuses on the creation of a Linux kernel module to query various MSRs to determine the virtualization features present in CPU. The module will then report the features it discovers as system message log.

#### Prerequisite: 
A machine capable of running Linux, with VMX virtualization features exposed.

#### Steps followed to complete the assignment:
1. First of all, install VMware Fusion to create virtual machines and then install Linux Ubuntu and enable Virtualization in the VM.
2. Fork the Linux repository:
https://github.com/torvalds/linux
3. Install git:
sudo apt-get install git
