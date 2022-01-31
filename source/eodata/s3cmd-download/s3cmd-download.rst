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
| 
