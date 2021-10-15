How to generate ec2 credentials?
================================

Before you attempt to perform the CLI operations, please assure that the necessary dependencies have been installed:

* Python-openstackclient FAQ
    
* (Strongly recommended) Virtualenv FAQ



EC2 are being used in getting access to the private bucket.
Users are able to generate ec2 credentials on their own by following those steps:



Log in to the Horizon Panel and click on the **API Access** in the Project branch.

.. figure:: https://raw.githubusercontent.com/CloudFerro/cf3-doc/main/source/s3/generateec2/ec2_1.png
   :scale: 100 %
   :align: center


Click on the **Download Openstack RC File**:

.. figure:: https://raw.githubusercontent.com/CloudFerro/cf3-doc/main/source/s3/generateec2/ec2_2.png

Choose **OpenStack RC File**:

.. figure:: https://raw.githubusercontent.com/CloudFerro/cf3-doc/main/source/s3/generateec2/ec2_3.png

Save your file on the hard disk and open your Terminal.

Type in commands presented below.

Virtual environment called **"openstack"** has been created for the FAQ purposes and consists of python-openstackclient packages.


.. code-block:: yaml

user@station:~$ workon openstack

(openstack) user@station:~$ source cloud_02722\ project_with_eo-openrc.sh

Please enter your OpenStack Password for project cloud_02722 project_with_eo as user john.doe@cloudferro.com:

(openstack) user@station:~$ openstack ec2 credentials create




