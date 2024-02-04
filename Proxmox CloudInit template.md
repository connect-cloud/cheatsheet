# Create a Proxmox template with CloudInit
## Download a cloud image
Get URL for Ubuntu Images from: https://cloud-images.ubuntu.com/

Download it to Proxmox using the GUI

## Create VM
Change the VM ID in commands below
```
qm create 1000 --memory 2048 --core 2 --cpu cputype=host --name ubuntu-24lts-template --net0 virtio,bridge=vmbr0
qm importdisk 1000 /var/lib/vz/template/iso/noble-server-cloudimg-amd64.img local-lvm
qm set 1000 --scsihw virtio-scsi-pci --scsi0 local-lvm:vm-1000-disk-0
qm set 1000 --ide2 local-lvm:cloudinit
qm set 1000 --boot c --bootdisk scsi0
qm set 1000 --serial0 socket --vga serial0
```
Edit the CloudInit settings in the Proxomox GUI
## Convert the VM to template
```
qm template 1000
```
