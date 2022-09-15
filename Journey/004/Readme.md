<!-- This is a template you can use for quick progress days. It removes a lot of the steps we encourage you to share in the longer template 000-DAY-ARTICLE-LONG-TEMPLATE.MD-->

# SSH into EC2 Instance whose key pair is lost

## Cloud Research
![Journey/004/Architecture-Diagram-Keypair-lost.png]
- ✍️ Tips Create temporary instance in the same availibility zone as original because you can attach volume from the same availibility zone 
- Stop the Original instance before you detach the volume as its the mount volume you cannot deattach it unless you stop the instance 
 
-  Place where SSH keys are placed on the volume

```
cat .ssh/authorized_keys 
```
-  List all the volumes attached to the instance 

```
lsblk
```
-  Make a new mount point, attach original volume and copy the keys and unmount

```
sudo mkdir /mnt/newvol
sudo mount -o nouuid /dev/xvdf1 /mnt/newvol
cp .ssh/authorized_keys /mnt/newvol/home/ec2-user/.ssh/authorized_keys
sudo umount /mnt/newvol
```
-  Change the volume device name and attach it to Original Ec2 instance 

## Social Proof

✍️ Show that you shared your process on Twitter or LinkedIn

[link](link)
