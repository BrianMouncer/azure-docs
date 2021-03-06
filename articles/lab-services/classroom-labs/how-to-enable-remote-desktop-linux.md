---
title: Enable remote desktop for Linux in Azure Lab Services | Microsoft Docs
description: Learn how to enable remote desktop for Linux virtual machines in a lab in Azure Lab Services.  
services: lab-services
documentationcenter: na
author: spelluru
manager: 
editor: ''

ms.service: lab-services
ms.workload: na
ms.tgt_pltfrm: na
ms.devlang: na
ms.topic: article
ms.date: 03/28/2019
ms.author: spelluru

---

# Enable and use remote desktop for Linux virtual machines in a lab in Azure Lab Services
This article shows you how to do the following tasks:

- Enable remote desktop for Linux VM
- How teacher can connect to the template VM via Remote Desktop Connection (RDP).
- How students connect to the student VM via RDP

## Enable remote desktop for Linux VM
During lab creation, teachers can enable **remote desktop connection** for **Linux** images. The **Enable Remote Desktop Connection** option is shown when a Linux image is selected for the template. When this option is enabled, teachers can connect to template VM and student VMs via RDP (Remote Desktop). 

> [!NOTE]
> Enabling **remote desktop connection** only opens the **RDP** port on Linux machines. You (as a teacher) have to install RDP and GUI packages in the template VM, and publish the template. 

![Enable remote desktop connection for a Linux image](../media/how-to-enable-remote-desktop-linux/enable-rdp-option.png)

## Teachers connecting to the template VM
Teachers see the **Remote Desktop** option to connect to the template VM at the time of creating the lab. 

![Connect to template via RDP at the time of creation](../media/how-to-enable-remote-desktop-linux/connect-at-creation.png)

You see the **Remote Desktop** option on the lab's home page after the lab is created and the template VM is started. Start the template VM if it's not started already. 

![Connect to template via RDP after the lab is created](../media/how-to-enable-remote-desktop-linux/rdp-after-lab-creation.png) 

When you select the **RDP** option, it downloads an RDP file. You open it to connect to the Linux machine. 

## Teachers connecting to a student VM
A lab owner (teacher/professor) can connect to a student VM by switching to the **Virtual Machines** view, and selecting the **connect** icon.

![Teachers connecting to the student VM](../media/how-to-enable-remote-desktop-linux/teacher-connect-to-student-vm.png)

## Students connecting to the student VM
1. When a student signs in to the Labs portal directly (`http://labs.azure.com`) or by using a registration link (`http://labs.azure.com/register/<registrationCode>`), a tile for each lab the student has access to is displayed. 
2. On the tile, select **Start** if the VM is stopped. 
3. Select **Connect**. This action downloads the RDP file on to your machine. Save it and open to connect to the Linux machine via RDP. 

    ![Student VM - RDP download](../media/how-to-enable-remote-desktop-linux/student-rdp-download.png)

    You can still connect to the Linux VM by using SSH. Select **... (ellipsis)** to see the SSH option. 
    
    ![Student VM - SSH](../media/how-to-enable-remote-desktop-linux/student-ssh.png)

    Copy and save the SSH connection string on the **Connect to your virtual machine** dialog box. Use this connection string from an SSH terminal (like [Putty](https://www.putty.org/)) to connect to the virtual machine. 

## Next steps
See the following articles:

- [As an admin, create and manage lab accounts](how-to-manage-lab-accounts.md)
- [As a lab owner, create and manage labs](how-to-manage-classroom-labs.md)
- [As a lab owner, set up and publish templates](how-to-create-manage-template.md)
- [As a lab user, access classroom labs](how-to-use-classroom-lab.md)

