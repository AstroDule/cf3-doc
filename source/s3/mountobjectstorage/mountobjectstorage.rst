How to mount object storage container as a file system in Linux using s3fs?
===========================================================================

If you want to create new Object Storage container you may check following guide: `LINK <https://cloudferro-cf3.readthedocs-hosted.com/en/latest/s3/objectstorage/objectstorage.html>`_

To mount your Object Storage container as file system do following steps:

Check if the s3fs is preinstalled on your virtual machine:

::

   eouser@vm1:~$ whereis s3fs
   s3fs: /usr/local/bin/s3fs

Provide access and secret key to the .passwd-s3fs file in your home directory:

::

   eouser@vm1:~$ echo access_key:secret_key>~/.passwd-s3fs

For obtaining ec2 credentials please follow this FAQ: `How to generate ec2 credentials? <https://cloudferro-cf3.readthedocs-hosted.com/en/latest/s3/generateec2/generateec2.html>`_ or send a request to the support by creating a new ticket in the https://creodias.eu.

Change the permissions for the file with stored credentials:

::

   eouser@vm1:~$ chmod 600 ~/.passwd-s3fs

Make an folder which you would like to use as mount place of the bucket:

::

   eouser@vm1:~$ mkdir directory

Mount a container using s3fs:

::

   eouser@vm1:~$ /usr/local/bin/s3fs testjohn directory -o passwd_file=~/.passwd-s3fs -o url=https://s3.waw3-1.cloudferro.com -o use_path_request_style -o umask=0002 -o allow_other
   
   
