# Installing proxmox on Topton machine.

Since pfSense will be the ruler of the entire network, it means that I will have to pass-trough all the network interfaces
to pfsense.

But how can you install pfSense if you pass-trough all network interfaces, you can't.

You can do this connected directly to the internet if you want from your own cable modem or whatever. I'm doing it from my current network.

My network from the Topton will be something like this:

![screenshot](/images/guides/Topton.png)

- Internet comes on Port 1
- Wireless Router on Port 2
- Living room Switch on Port 3
- Office switch on Port 4

Now I'm regretting not buying a Topton with 6 ports.

So basically all the ports will be dedicated to something. This means that we will have to pass-trough all of the,

### Install proxmox

Connect the network to the last port of the Topton mini-pc, and install proxmox as usual. Just next next and next.

