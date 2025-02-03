# Installing proxmox on Topton machine.

Since pfSense will be the ruler of the entire network, it means that I will have to pass-trough all the network interfaces
to pfsense.

But how can you install pfSense if you pass-trough all network interfaces, you can't.

You can do this connected directly to the internet if you want from your own cable modem or whatever. I'm doing it from my current network.

My network from the Topton will be something like this:

![screenshot](/images/guides/topton/Topton_diagram.png)

- Internet comes on Port 1
- Wireless Router on Port 2
- Living room Switch on Port 3
- Office switch on Port 4

Now I'm regretting not buying a Topton with 6 ports.


### Install proxmox

Connect the network/internet to the last port of the Topton mini-pc, and install proxmox as usual. Just next next and next.

And you should have something like this:
![screenshot](/images/guides/topton/proxmox_network.png)

Now since I want port 1 to be my internet, I'm going to connect a cable on that port, pass-trough the first 3 ports to pfsense and install it.

To note that I'm not attaching vmbr0 to the VM of pfsense, I'm only passing the network ports

I'm only going to define the wan port during the installation, not the lan, that is for later.

After installing you should have something like this:
![screenshot](/images/guides/topton/pfsense_installed.png)

When going trought the web configurator for the first time don't choose this option: ``Block RFC1918 Private Networks``,
unless you are accessing it trough your public ip, if you are not you are going to block yourself, which is wonderful!

Also don't forget to activate AES on System -> Advanced -> Miscellaneous -> Cryptographic & Thermal Hardware

Next is time to setup our LAN