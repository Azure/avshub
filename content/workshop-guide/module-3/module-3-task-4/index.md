---
title: "Module 3 Task 4"
linkTitle: "Task 4: Configure SRM Site Pairing"
weight: 5

description: >
  Task 4: Configure a Site Pairing in Site Recovery Manager
---
## **SRM Site Pairing**

>Remember X is your group number, Y is your participant number, Z is the SDDC you've been paired with.

In this task you will pair the protected site GPSUS-PARTNER**X**-SDDC and the recovery site GPSUS-PARTNER**Z**-SDDC.

### **Exercise 1: Site Pairing**

Site pairing can be configured from vCenter on either the primary or the recovery private cloud. You will work on the primary site’s vCenter.


#### Step 1: Access Site Recovery Manager from vCenter Server

![](Mod3Task4Pic1.png)

1. Log into vCenter Server in the primary AVS private cloud GPSUS-PARTNER**X**-SDDC and click the menu bat.
2. Select **Site Recovery** from the main menu.

![](Mod3Task4Pic2.png)

Click **OPEN Site Recovery**.

#### Step 2: Create New Site Pair

![](Mod3Task4Pic3.png)

Click **NEW SITE PAIR**.

#### Step 3: Select local vCenter Server

![](Mod3Task4Pic4.png)

1. Ensure your local vCenter Server is selected.
2. Ensure **Pair with a peer vCenter Server located in a different SSO domain** is selected.
3. Click **NEXT**.

#### Step 4: Peer vCenter Server

![](Mod3Task4Pic5.png)

1. Enter the vCenter Server information for the Recovery site. This should be GPSUS-PARTNER**Z**-SDDC.
2. Click **FIND VCENTER SERVER INSTANCES**. If a warning shows up click **CONNECT**.
3. Select your peer vCenter Server.
4. Click **NEXT**.

#### Step 5: Select services identified

![](Mod3Task4Pic6.png)

1. Select the top checkbox to select all services.
2. Click **NEXT**. Then click **FINISH**.

#### Step 6: Confirm Site Pairing Completes

![](Mod3Task4Pic7.png)

When the configuration process completes, the SRM main page displays the new site pairing.
