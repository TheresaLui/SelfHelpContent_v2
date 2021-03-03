<properties
	pageTitle="Large Files on Linux"
	description="Large Files on Linux"
        service="Microsoft.Storage"
        resource="Microsoft.Storage/storageAccounts"
	authors="rimayber"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="ccdda5e7-d282-4efe-926d-ecf40985649a"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Large Files on Linux

1. When running an upload from Linux, that involves just a small number of large files (e.g. one 500 GB file), AzCopy can perform slowly.
2. The root cause is that AzCopy reads files sequentially... but, some Linux distros aren?t tuned for optimal sequential read performance of very large files. 
3. In particular, Linux distros are commonly configured to pre-read only 128 KB. 
4. That?s not enough for the kind of work AzCopy does. 
5. The solution is simply to increase Linux?s pre-read size, for the device in question.
6. So, for disk /dev/sdc for example, here?s how you could do it:

~~~shell

echo 8192 | sudo tee -a /sys/block/sdc/queue/read_ahead_kb

~~~

7. We've tested several values. 4096 is also OK, but was slightly slower.

*Note: that if you only do the above, the setting won?t persist after reboots. To make it persistent, you have to script it to be run at startup, typically with systemd on recent distros (such as recent Ubuntu versions) and with /etc/rc.d/rc.local on older ones. (Remove ?sudo? from the script when automating it for use at startup).*

## Recommended Documents

1. [Performance Large files in general](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD/265496/AzCopy-v10?anchor=performance-moving-large-files) for more info. 
