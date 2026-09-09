###### Striping with Distributed Parity

RAID 5 combines striping (like RAID 0) with distributed parity.

Distributed parity: The info that can correct errors if a disk is broken is stored in all disks in the array. This means that if one disk is damaged the data can still be recoved as long as there is still one working disk. 

Offers great READ unless a disk is damaged 