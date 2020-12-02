# Linux Commands

#### Physical Volumes, Volume Groups, Logical Volumes

| Syntax | Description |
| ---- | ------------- |
| vgcreate \<name> <list of physical/virtual disk volumes> | Create volume groups |
| vgs | Display the list of volume groups with Size and Availability |
| vgdisplay -vvvv | Display comprehensive detail of volume group. Information will be appended with every v.|
| lvcreate -L \<Size> -n \<name> <volume-group> | Create a logical volume under volume group |
| lvs | Display the list of logical volumes |
| lvdisplay -m | Display the logical volume with mapping physical drive |
| lvremove \<volume-group>/\<name>| Removes the logical volume|
| pvs | Lists the physical volumes |