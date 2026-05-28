# Install on Workstation


## Hyper-V



## Workstation

I am going to build this as a VM under VMWare Workstation, just for testing.

I need to be able to use it for later, more complex exercises, so its important to call it pve21 and give it an IP address with .21 as the last octet.

I make sure to enable nested virtualization (Virtualize Intel VT-x). In recent times, it can be messy to make this work, check my VMWare Workstation notes for some hints.

<figure>
<img src = "https://jor-donegal.github.io/Proxmox26/images/fig2.jpg">
<figcaption>Fig 2. VMWare Processors.</figcaption>
</figure>

I used Debian 12 as VM type.

If you are installing on bare metal, the process will be the same, just without the VMWare activities.

I download the Proxmox ISO, 8.4.