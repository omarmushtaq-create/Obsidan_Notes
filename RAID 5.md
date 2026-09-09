###### Striping with Distributed Parity

RAID 5 combines striping (like RAID 0) with distributed parity.

Distributed parity: The info that can correct errors if a disk is broken is stored in all disks in the array. This means that if a disk is damaged the data can still be recoved as long as there is only one broken disk. 

Offers great READ unless a disk is damaged becuase the system needs to use the parity information to recover data.

Write is slower because of the need to calculate parity. 

min 3 disks max is set in OS, you want a middle ground because more disks = higher chance one of them fails. 