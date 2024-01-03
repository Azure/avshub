---
title: "Module 2 Task 4"
linkTitle: "Task 4: Deploy HCX"
weight: 5

description: >
  Task 4: Deploy the HCX OVA to On-Premises vCenter
---

## **Deploy HCX OVA**

In this step, we will deploy the HCX VM with the configuration from the [On-Premises VMware Lab Environment](/docs/#on-premises-vmware-lab-environment) section.

{{< alert color="success" >}}
You will perform the instructions below from the On-premises VMware Environment
{{< /alert >}}

### Step 1: Deploy HCX connector VM

#### **If Option 1**: Deploy OVA from download.

![Deploy OVF Template from download](Mod2Task4Pic1.png)

1. Right-click **Cluster-1**.
1. Click **Deploy OVF Template**.

![Select the OVA Template](Mod2Task4Pic2.png)

3. Click the button to point to the location of the downloaded OVA for HCX.
1. Click **NEXT**.

#### **If Option 2**: Deploy HCX from Content Library

![Create new VM from Template](Mod2Task4Pic6.png)

1. Once the import is completed from the previous task, click **Templates**.
1. Right Click the imported HCX template.
1. Click **New VM from This Template**.

![Select a Name and Folder](Mod2Task4Pic7.png)

4. Give your HCX Connector a name: **HCX-OnPrem-X-Y**, where X is your group number and Y is your participant number.
1. Click **NEXT**.

### Step 2: Name the HCX Connector VM

![Name the HCX Connector VM](Mod2Task4Pic3.png)

1. Give your HCX Connector a name: **HCX-OnPrem-X-Y**, where X is your group number and Y is your participant number.
2. Click **NEXT**.

### Step 3: Assign the network to your HCX Connector VM

![Assign the network to your HCX Connector VM](Mod2Task4Pic4.png)

Keep the defaults for:
- Compute Resource
- Review details
- License agreements (Accept)
- Storage (LabDatastore)

1. Click to select **management** network.
2. Click **NEXT**.

### Step 4: Customize template

![Customize template](Mod2Task4Pic5.png)

| **Property**                            | **Value**                                                                                                              |
|-----------------------------------------|------------------------------------------------------------------------------------------------------------------------|
| Hostname                                | Suggestion: HCX-OnPrem-**X**-**Y**) **Note: Do not leave a space in the name as this causes the webserver to fail)** |
| CLI "admin" User Password/root Password | MSFTavs1!                                                                                                           |
| Network 1 IPv4 Address                  | 10.**X**.**Y**.9                                                                                                         |
| Network 1 IPv4 Prefix Length            | 27                                                                                                                     |
| Default IPv4 Gateway                    | 10.**X**.**Y**.1                                                                                                         |
| DNS Server list                         | 1.1.1.1                                                                                                                |

### Step 5: Validate deployment

Once done, navigate to Menu \> **VM's and Templates** \> **Power on** the newly created HCX Manager VM. 

> The boot process may take 10-15 minutes to complete.