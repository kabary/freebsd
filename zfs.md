### How to create a zpool with two disks?

`zpool create archive-pool da1 da2 `

You can run `df` to see where the pool is mounted by default.

`cd /archive-pool`

### How to list all the current zpools?

`zpool list`

### How to create a ZFS dataset (filesystem)?

`zfs create archive-pool/backup1`

### How to unmount/mount a ZFS dataset?

`zfs umount archive-pool/backup1`

`zfs mount archive-pool/backup1`

### How to see the mountpoint of a ZFS dataset?

`zfs get mountpoint archive-pool/backup1`

### How to set a new mountpoint for a ZFS dataset?

`zfs set mountpoint=/mnt/backup1 archive-pool/backup1`

### How to delete a ZFS dataset?

`zfs destroy archive-pool/backup1`

### How to delete a zpool?

`zpool destroy archive-pool`

### How to create a ZFS dataset snapshot?

`zfs snapshot archive-pool/backup1@today`

### How to list ZFS snapshots?

`zfs list -t snapshot`

### How to rollback to a snapshot?

`zfs rollback archive-pool/backup1@today`

### How to check the status of all the pools?

`zpool status -x`

### Scrubbing to check I/O errors and verify data integrity on pools?

`zpool scrub archive-pool`

`zpool status archive-pool`

### How to clear zpool errors?

`zpool clear archive-pool/backup1`

### How to replace a disk in a running pool?

`zpool replace archive-pool da1 da2`






