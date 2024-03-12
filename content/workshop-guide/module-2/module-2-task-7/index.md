---
title: "Module 2 Task 7"
linkTitle: "Task 7: Configure HCX"
weight: 8

description: >
  Task 7: Configure HCX and connect to vCenter
---

{{< alert color="success" >}}
You will perform the instructions below from the On-premises VMware Environment
{{< /alert >}}

## Configure On-Premises HCX

In this section, we will integrate and configure HCX Manager with the On-Premises vCenter Server.

### Step 1: Connect vCenter Server

![Connect your vCenter Server](Mod2Task7Pic1.png)

1. In **Connect your vCenter**, provide the FQDN or IP address of on-premises vCenter server and the appropriate credentials.
    * vCenter IP: <https://10.X.Y.2>
    * Username: `administrator@avs.lab`
    * Password: `MSFTavs1!`
2. Click **CONTINUE**.

### Step 2: Configure SSO/PSC

![Configure SSO/PSC](Mod2Task7Pic2.png)

1. In **Configure SSO/PSC**, provide the same vCenter IP address: <https://10.X.Y.2>
2. Click **CONTINUE**.

### Step 3: Restart HCX Appliance

![Restart HCX appliance to save changes](Mod2Task7Pic3.png)

Verify that the information entered is correct and select **RESTART**.

{{% alert title="The Reboot process might take up to 15 minutes" color="warning" %}}  
The reboot process might take between 10 to 15 minutes. Keep checking every 3-4 minutes to ensure you can get to HCX Manager.
{{% /alert %}}

![HCX configuration dashboard after restart](Mod2Task7Pic4.png)

1. After the services restart, you'll see vCenter showing as **Green** on the screen that appears. Both vCenter and SSO must have the appropriate configuration parameters, which should be the same as the previous screen.
2. Next, click on Configuration to complete the HCX configuration.

![Edit the HCX Administrator role mapping configuration](Mod2Task7Pic5.png)

1. Click **Configuration**.
2. Click **HCX Role Mapping**.
3. Click **Edit**.
4. Change User Groups value to match lab SSO configuration: `avs.lab\Administrators`
5. **Save** changes.

> Please note that by default HCX assigns the HCX administrator role to "vsphere.local\Administrators". In real life, customers will have a different SSO domain than **vsphere.local** and needs to be changed. This is the case for this lab and this needs to be changed to **avs.lab**.

{{% alert color="warning" %}}  
It may take an additional 5-10 minutes for the HCX plugins to be installed in vCenter, log back out and log back in if it does not show up automatically.
{{% /alert %}}