Welcome
-------

Welcome to F5's Service Provider SP Event IoT hands on training series.
The goal of this lab is to show you how F5 BIG-IP native functionalities of AFM, PEM and DNS together can be used to build a solution which can provide network-based security for Internet of Things (IoT) services. This lab will combine together functionalities from AFM (Firewalling Policies) PEM (Session DB, as well as reporting), and DNS queries processing (coming from DNS module) to show how we can exploit the interaction between modules within our consolidated BIG-IP solution.


Getting Started
---------------

Connect F5 UDF Web Portal at udf.f5.com, login using your usual F5 credentials and go to Courses. Search for IoT, you will find the Course: IoT Training: SP Specialization Event

.. NOTE::
	All work for this lab will be performed exclusively from the Linux Jumphost and Linux Client Machines. All required access and servies needed to perform classes and labs are provided by the UDF. No installation or interaction with your local system is required.

Prerequisites
-------------

In order to complete this series of training classes you will need to utilize
the provided blueprint for the course session. To access the UDF sessions you will
need to have the following prerequists met. 

- Current Access to UDF
- SSH key of your access machine in UDF
- Windows or MAC ssh client working with UDF


All pre-built environments implement the :ref:`lab-topology` shown below.

UDF Blueprint
~~~~~~~~~~~~~~~~~

Please follow the instructions provided by your lab instructor to access your
lab environment. The lab environment will be delivered  via UDF blueprints to 
each student.

.. NOTE:: Please deploy and start your lab as soon as you have access to the class as the lab takes some time to boot all the components.


Lab Topology
------------

The network topology implemented for this lab based on the Service Provider Gi lan
path. The focus of the lab is Control Plane programmability and Data Plane elements,
so this lab will focus at both parts at different time.
The following components have been included in your lab environment:

-  1 x ``F5 BIG-IP VE`` (v13.0 HF2)

-  1 x Linux Jumphost (ubuntu 16.04 - mate)

-  2 x Linux Clients (ubuntu 16.04 - mate)

-  1 x Linux Server (ubuntu 16.04)

.. _lab-topology:

|lab_topo1|


The following table lists VLANS, IP Addresses and Credentials for all
components:

.. csv-table:: Lab Network Information
    :header: "Component", "VLAN", "IP Address", "Credentials"
    :widths: 40, 40, 40, 60

    "Linux Jumphost", "Mgmt", "10.1.1.20", ""
    "BIG-IP", "Mgmt", "10.1.1.4", "admin/admin"
    "", "Internal", "10.1.10.5", ""
    "", "External", "10.1.20.5", ""
    "", "Control", "10.1.30.5", ""
    "Client 00", "Mgmt", "10.1.1.9", "udfclient/S3rv1ceP0weR"
    "", "Internal", "10.1.10.25", ""
    "Client 01", "Mgmt", "10.1.1.7", "udfclient/S3rv1ceP0weR"
    "", "Internal", "10.1.10.30", ""
    "ELK Stack", "Mgmt", "10.1.1.5", "ubuntu/default"
    "", "Control", "10.1.30.15", ""

.. |lab_topo1| image:: /_static/lab_topology.png
   :width: 8in
   :height: 4in


