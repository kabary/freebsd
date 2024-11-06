### How to create a zpool with two disks?

`zpool create archive-pool da1 da2 `

You can run `df` to see where the pool is mounted by default.

`cd /archive-pool`

### How to list all the current zpools?

`zpool list`

### How to create a ZFS dataset (filesystem)?

`zfs create archive-pool/backup1`

### How
