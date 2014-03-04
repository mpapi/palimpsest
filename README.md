Manages a copy-on-write filesystem backed by loopback devices, using
`dmsetup(1)` and `losetup(1)`.

For example, you can:

* create a filesystem image in a sparse file and mount it
* write some data to it and unmount it
* create a "layer" file backed by the data you just wrote and mount that
* make some changes to data you write, then umount and destroy the layer
* mount the base file again, see that no changes were made
