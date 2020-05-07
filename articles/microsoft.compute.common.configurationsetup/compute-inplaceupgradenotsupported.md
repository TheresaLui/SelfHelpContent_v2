<properties
    pageTitle="Cannot perform an in-place upgrade for my VM"
    description="Cannot perform an in-place upgrade for my VM"
    service="microsoft.compute"
    resource="virtualmachines"
    authors="ScottAzure"
    ms.author="scotro"
    displayOrder=""
    selfHelpType="generic"
    supportTopicIds="32725647,32725646"
    resourceTags=""
    productPesIds="14749,15571,15797,16454,16470"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    articleId="a6795daa-1699-4018-a759-34e0a727bad9"
	ownershipId="Compute_VirtualMachines_Content"
/>

# Cannot perform an in-place upgrade for my VM

4 out of 5 customers resolved their in-place upgrade issues of their VM using the steps below.<br>

## **Recommended Steps**

Consider the following scenario:<br>

* You have a virtual machine (VM) that is running Microsoft Windows in a Microsoft Azure environment.<br>
* You run an in-place upgrade of the VM to a newer version of the operating system.

In this scenario, the upgrade may fail or become blocked and require direct console access to unblock it.<br>

**For Windows upgrades**, [performing an in-place system upgrade is not supported on Windows-based Azure VMs](https://support.microsoft.com/help/4014997)<br>

**For Linux major upgrades**, a similar scenario could occur. Please work with your distro vendor to understand next steps.<br>

## **Recommended Documents**

* [Performing an in-place system upgrade is not supported on Windows-based Azure VMs](https://support.microsoft.com/help/4014997)
