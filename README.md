# vm-gpu-passthrough

## GUIDE
 - add `vfio-pci.ids=1002:6660` as a kernel argument
 - go to /etc/modprobe.d/ and add a file to do the thing about vfio
 - add to the start of `MODULES` in `/etc/mkinitcpio.conf` the modules `vfio_pci vfio vfio_iommu_type1 vfio_virqfd ` and `modconf` int the `HOOKS`
 - for more details go to `https://wiki.archlinux.org/index.php/PCI_passthrough_via_OVMF#Isolating_the_GPU`
