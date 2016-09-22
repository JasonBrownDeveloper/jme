Linux Driver for the JMicron(R) JMC250/JMC260 PCI-E Ethernet Adapter
====================================================================

Contents
========

- Readme First
- Building and Installation
- Command Line Parameters
- Known Issues

Readme first
============

This file describes the Linux Driver for the JMicron(R) JMC250/JMC260 PCI-E Ethernet
Adapter. Version 1.0.8.5 supports the 2.6.16 or above kernels.

Install Requirement:
1. Kernel srource HEAD
2. Compiler

Building and Installation
=========================

Install Process:

1. Clone jme-1.0.8.5

        # git clone https://github.com/JasonBrownDeveloper/jme.git

2. Change directory to jmebp-1.0.8.5

        # cd jmebp-1.0.8.5

3. Compile driver with root permission

        # make install
   The binary will be installed as:  
   /lib/modules/`<KERNEL VERSION>`/kernel/drivers/net/jme.ko

4. Load the driver:

        # modprobe jme

Command Line Parameters
=======================

1. Assign an IP address, where x is the interface number:

        # ifconfig ethx <IP_address>

Known Issues
============

The JMC25x/JMC26x Gigabit Ethernet Chip is not IEEE 802.3az compliant and gigabit will not connect if the feature is enabled on the remote device.

