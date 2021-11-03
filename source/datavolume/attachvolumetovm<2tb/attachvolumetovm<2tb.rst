How to attach a volume to VM (<2 TB) on Linux?
==============================================


If the volume does not exist yet, it must be created. Go to Horizon, „`volumes” <https://horizon.cloudferro.com/project/volumes/>`_, click „create volume”. Give it an appropriate name, select size and disk type (either HDD-default or SSD).

Now, from the volume menu, select „manage attachments” and attach the volume to the desired instance. It becomes visible in it as a block device, like /dev/vdb or /dev/sdb (depending on what disk type we choose).

If the volume had not been used before (it has been freshly created), it must be first partitioned and formatted, e.g
