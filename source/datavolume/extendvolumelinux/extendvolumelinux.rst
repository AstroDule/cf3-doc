How to extend the volume (Linux)?
==================================

It is possible to extend the Volume from Horizon dashboard.

Another method is to create a new volume, attach it to the VM, copy all the data from the old volume to the new one, check if the data is properly copied, then detach and delete the old one. Not all filesystems are resizable.

.. warning::

   1. It is strongly recommended to backup the volume by creating Volume Snapshot before proceeding with extending the volume.
   
.. warning::

   2. If you have a volume < 2TB and you want to extend it above 2TB, please do not follow below instructions. Instead please create a new volume, format it according to another article: `HOW TO ATTACH A VOLUME TO VM (>2TB) ON LINUX? <https://creodias.eu/-/how-to-attach-a-volume-to-vm-2tb-linux->`_, attach it to the VM, copy the data from the old volume to the new one, check if it is fully copied, detach and delete the old volume.
   
   
