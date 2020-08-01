# vm-gpu-passthrough

## GUIDE
 - add `intel_iommu=on iommu=pt` to kernel argument
 - add `vfio-pci.ids=1002:6660` as a kernel argument (optional)
 - in the file /etc/modprobe.d/vfio.conf put `options vfio-pci ids=1002:6660`
 - add to the start of `MODULES` in `/etc/mkinitcpio.conf` the modules `vfio_pci vfio vfio_iommu_type1 vfio_virqfd ` and `modconf` int the `HOOKS`
 - for more details go to `https://wiki.archlinux.org/index.php/PCI_passthrough_via_OVMF#Isolating_the_GPU`
