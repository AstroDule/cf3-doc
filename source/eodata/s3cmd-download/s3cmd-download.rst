How to download EODATA products using s3cmd?
====
| **Establishing connection**
|LIST EODATA USING BOTO3?
| At first, please verify your connection with EODATA bucket by using list command.
::

  eouser@vm01:~$ s3cmd ls
|
| You should obtain this output.
::

  2017-11-15 10:40  s3://DIAS
  2017-11-15 10:40  s3://EOCLOUD
  2017-11-15 10:40  s3://EODATA
  2017-11-15 10:40  s3://HRSI
|
| If you have encountered any problems, please check all steps from this tutorial.
| `How to access EODATA and Object storage using s3cmd? <https://cloudferro-cf3.readthedocs-hosted.com/en/latest/datavolume/accessusings3cmd/accessusings3cmd.html>`_
|
| **Downloading EOData product**
| Entire product is being structured in a whole directory, not a single file. Therefore, you have to use –recursive parameter in order to avoid any “skipping” of files.
| Example for downloading a Sentinel-2 product:
::

  s3cmd get --recursive s3://EODATA/Sentinel-2/MSI/L2A/2022/01/30/S2B_MSIL2A_20220130T115209_N0400_R123_T28SFB_20220130T125446.SAFE/
|
| The above command will download *S2B_MSIL2A_20220130T115209_N0400_R123_T28SFB_20220130T125446.SAFE* product to your local folder from which you are issuing the command.
|
| Files can be also redirected to specific local folder. For our purposes it would be a *downloads* directory. Join path to local folder at the end of command.
::

  eouser@vm01:~$ mkdir downloads
  eouser@vm01:~$ s3cmd -d get --recursive s3://EODATA/Sentinel-2/MSI/L2A/2022/01/30/S2B_MSIL2A_20220130T115209_N0400_R123_T28SFB_20220130T125446.SAFE/ downloads/
