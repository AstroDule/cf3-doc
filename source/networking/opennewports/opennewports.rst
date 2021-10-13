How can I open new ports (i.e. port 80 for http) for my service/instance?
=========================================================================

To open new port for new service on the instance, click Project -> Network -> Security Groups and click "Create Security Group".

By default on the new group you will have two Egress (outgoing) rules, for ipv4 and ipv6.

You need to create new Ingress (incoming) rule that should look like this:

``Ingress    IPv4    TCP    80 (HTTP)    0.0.0.0/0``


After creating the new Security Group you have to add it to your instance.

In the instance settings click "Security Groups" and add your newly created Security Group to your instance.
