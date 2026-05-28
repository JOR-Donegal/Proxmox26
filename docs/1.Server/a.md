# Install on Hyper-V

I already have an internal switch with domain controllers from a previous exercise. I use this.
I power up one domain controller and check that I have working DHCP.

<figure>
<img src = "https://jor-donegal.github.io/Proxmox26/images/fig1.jpg">
<figcaption>Fig 1. Recce.</figcaption>
</figure>


I assume you are very familiar with Hyper-V

I create a VM called __Proxmox__ as my gold image.

I specify 

1. Generation 1
2. 4096 MB of DRAM with dynamic memory


Everything else is at defaults.

After the VM is created, I go to settings and

1. Increase the number of processors to 2.
2. I disable checkpoints.

Next I need to enable nested virtualization. Check the settings of the VM.

````
Get-VMProcessor -VMName "proxmox" | Format-List *
````

Set host to expose virtualization extensions. 

````
Set-VMProcessor -VMName "proxmox" -ExposeVirtualizationExtensions $true
````
Use the first command again to check to see if that worked.

I download the Proxmox ISO, 8.4. I have problems running 9.x on Hyper-V.
