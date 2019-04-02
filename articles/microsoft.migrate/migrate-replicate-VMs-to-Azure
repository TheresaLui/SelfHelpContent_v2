<properties
	pageTitle="Azure Migrate preview - Replicate VMs to Azure"
	description="Azure Migrate preview - Replicate VMs to Azure"
	service="microsoft.migrate"
	resource="projects"
	authors="shijojoy"
	ms.author="shijoy"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32631950"
	resourceTags=""
	productPesIds="16348"
	cloudEnvironments="public"
	articleId=""
/>

# Azure Migrate preview - Replicate VMs to Azure

## **Recommended Steps**

### **What is the data replication path of the VMs?**
The path is DataStore -> ESXi host -> Appliance -> Azure Storage. We connect to the vCenter using VDDK read and then vCenter redirects the call to an ESXi host.

### **For large scale migrations, is it possible to add multiple appliances for better performance? And does the sizing remain the same for large number of migrations?**
Currently we do not support Scale-up or Scale-out of Migration appliance. We plan to support this in near future.

### **Since the migration appliance uses port 443 for replication, is it supported to do this over a VPN or ER connection?**
Yes, this can be over an ER with Public Peer/Microsoft Peer. S2S VPN is not supported

### **What is the frequency of VM snapshot creation?**
The frequency of snapshot creation is dependent on previous cycle time, limited to a maximum of 1 per hour per VM except for the planned migration cycle which is an on demand replication cycle that happens as part of VM migration. It is dynamically calculated and cannot be changed.

### **What is the performance impact on the production VMs during the snapshot operations?**
Perf impact will be same as prescribed by Vmware during snapshot phase. It depends on various factors:
a.	IOPS headroom on SAN
b.	Churn on the VM

### **If the VMware VM contains data disks encrypted, is there a way for the appliance to proactively identify and report that to disable it? Is that part of the pre-check?**
Currently we are unable to detect this.

### **For the replication traffic, the appliance does not provide any throttling settings, what is the default behavior, as in, does it take the maximum bandwidth possible?**
Take the maximum bandwidth possible. However, Appliance is a Windows appliance, so you can use Windows NetQoS to restrict n/w upload throughput. Please keep in mind though that setting this too low would mean longer upload cycles and therefore longer duration during which the VM disk snapshot will be live.

### **What certificate does the appliance use to protect the replication traffic?**
All replication traffic is sent over https(SSL/TLS) to Azure storage.

### **Is there an option to pause/resume the replication?**
No, because that would involve increasing the snapshot active time causing impact to the production VMs. However, a cancel current transfer feature is in the backlog.

### **If replication fails due to a certain reason and needs to be performed again: Does the second replication makes use of the existing data?
**
There are two cases here: 
1.	Where some disks succeeded in their upload -> For these disks, the consecutive retry of the cycle would upload lesser data.
2.	For the failed disks, it would upload the whole data again as the underlying snapshot has changed and hence, we cannot reuse the previously uploaded data.
