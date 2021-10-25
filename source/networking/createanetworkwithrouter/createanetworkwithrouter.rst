How to create a network with router in Horizon Dashboard?
========================================================

When you create a new project in Horizon, its content is empty. You have to manually configure your private network. In order to complete this task, please follow those steps.

 

| 1. Log in to your OpenStack dashboard and choose **Network** tab, then choose **Networks** sub-label.

.. figure:: https://raw.githubusercontent.com/CloudFerro/cf3-doc/main/source/networking/createanetworkwithrouter/net1.png
   :align: center
|
|
| 2. Click on the **“Create Network”** button.

.. figure:: https://raw.githubusercontent.com/CloudFerro/cf3-doc/main/source/networking/createanetworkwithrouter/net2.png
   :align: center
|
|
| 3. Define your Network Name and tick two checkboxes: **Enable Admin State** and **Create Subnet**. Go to Next.

.. figure:: https://raw.githubusercontent.com/CloudFerro/cf3-doc/main/source/networking/createanetworkwithrouter/net3.png
   :align: center
|
|
| 4. Define your Subnet name. Assign a valid network address with mask presented as a prefix. (This number determines how many bytes are being destined for network address)

| Define Gateway IP for your Router. Normally it’s the first available address in the subnet.

| Go to Next.

.. figure:: https://raw.githubusercontent.com/CloudFerro/cf3-doc/main/source/networking/createanetworkwithrouter/net4.png
   :align: center
|
|
| 5. In Subnet Details you are able to turn on DHCP server, assign DNS servers to your network and set up basic routing. In the end, confirm the process with **“Create”** button.

.. figure:: https://raw.githubusercontent.com/CloudFerro/cf3-doc/main/source/networking/createanetworkwithrouter/net5.png
   :align: center
|
|
| 6. Click on the **Routers** tab.

.. figure:: https://raw.githubusercontent.com/CloudFerro/cf3-doc/main/source/networking/createanetworkwithrouter/net6.png
   :align: center
|
|
| 7. Click on the **“Create Router”** button.

.. figure:: https://raw.githubusercontent.com/CloudFerro/cf3-doc/main/source/networking/createanetworkwithrouter/net7.png
   :align: center
|
|
| 8. Name your device and assign the only available network → external. Finish by choosing **“Create Router”** blue button.

.. figure:: https://raw.githubusercontent.com/CloudFerro/cf3-doc/main/source/networking/createanetworkwithrouter/net8.png
   :align: center
|
|
| 9. Click on your newly created Router (e.g called “Router_1”).


.. figure:: https://raw.githubusercontent.com/CloudFerro/cf3-doc/main/source/networking/createanetworkwithrouter/net9.png
   :align: center
|
|

| 10. Choose **Interfaces**.

.. figure:: https://raw.githubusercontent.com/CloudFerro/cf3-doc/main/source/networking/createanetworkwithrouter/net10.png
   :align: center
|
|
| 11. Choose **+ Add Interface** button.


.. figure:: https://raw.githubusercontent.com/CloudFerro/cf3-doc/main/source/networking/createanetworkwithrouter/net11.png
   :align: center
|
|
| 12. Assign a proper subnet and fill in IP Address. (It’s the gateway for our network). Submit the process.


.. figure:: https://raw.githubusercontent.com/CloudFerro/cf3-doc/main/source/networking/createanetworkwithrouter/net12.png
   :align: center
|
|
| 13. The internal interface has been attached to the router.


.. figure:: https://raw.githubusercontent.com/CloudFerro/cf3-doc/main/source/networking/createanetworkwithrouter/net13.png
   :align: center
|
|

