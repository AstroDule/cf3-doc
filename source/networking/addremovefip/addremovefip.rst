How to Add/Remove Floating IP’s to your VM?
===========================================


In order to make your VM accessible from the Internet, you need to use Floating IP’s. Floating IP’s in Openstack are public IP addresses assigned to your Virtual Machine. Floating IP assignment allows you (when you have Security Groups set properly) to host services like SSH, HTTP or other over the Internet.



| **How to assign a Floating IP to your VM:**
| In Instances tab in Horizon, click the dropdown menu next to your VM and choose „Associate Floating IP”

.. figure:: https://raw.githubusercontent.com/CloudFerro/cf3-doc/main/source/networking/addremovefip/fip1.png
   :align: center

You will be shown a window like this one:

.. figure:: https://raw.githubusercontent.com/CloudFerro/cf3-doc/main/source/networking/addremovefip/fip2.png
   :align: center
   
You may choose an address from the dropdown menu, but if it's empty, you need to allocate an address first. Click "+" icon on the right.

.. figure:: https://raw.githubusercontent.com/CloudFerro/cf3-doc/main/source/networking/addremovefip/fip3.png
   :align: center

.. figure:: https://raw.githubusercontent.com/CloudFerro/cf3-doc/main/source/networking/addremovefip/fip4.png
   :align: center
   
Click "Allocate IP".

.. figure:: https://raw.githubusercontent.com/CloudFerro/cf3-doc/main/source/networking/addremovefip/fip5.png
   :align: center

Select newly allocated IP address and click Associate.

.. note::
   
   The IP address should be associated with a local address from "192.168.x.x" subnet. If you have "10.x.x.x" address change it to "192.168.x.x" address.
   
   
Click "Associate".

 
.. note::

   The VM's communicate between themselves trough internal network "192.168.x.x" so if you are connecting from one Virtual Machine to another 
   you should use private addresses. If you try to connect your VM to the wrong network you will be notified by the following the message.
   
 
.. figure:: https://raw.githubusercontent.com/CloudFerro/cf3-doc/main/source/networking/addremovefip/fip6.png
   :align: center
 


You now have public IP assigned to your instance and visible in Instances menu:

.. figure:: https://raw.githubusercontent.com/CloudFerro/cf3-doc/main/source/networking/addremovefip/fip7.png
   :align: center

You can now connect to your Virtual Machine trough SSH or RDP from the Internet.


   



