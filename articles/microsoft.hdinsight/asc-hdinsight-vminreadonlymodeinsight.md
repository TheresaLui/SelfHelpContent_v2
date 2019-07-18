<properties
    ms.author="v-anreg"
    pageTitle="VM is in read-only mode"
    description="Virtual Machine Issue"
    infoBubbleText="VM has booted up in read-only mode. See details on the right."
    service="microsoft.hdinsight"
    resource="clusters"
    authors="anirudhrege"
    displayOrder=""
    articleId="Hdi_VirtualMachine_ReadOnlyMode"
    diagnosticScenario="HDInsightReadOnlyFileSystemInsight"
    selfHelpType="diagnostics"
    supportTopicIds="32636433,32636481"
    resourceTags=""
    productPesIds="15078"
    cloudEnvironments="public"
/>

# We ran diagnostics on your resource and found the following issue

The virtual machine booted up with a read-only file system. The following node(s) are in read-only mode: <!--$AlertHost-->[AlertHost]<!--/$AlertHost--> <br>
The drive has to be remounted in read-write mode.

## **Recommended Steps**

1. Run the following command to identify the read-only disk with drive and partition:
```
        mount -l | grep sd
```
2. SSH into the node and run the following commands to change it to read/write mode:
 ```       
        sudo fsck.ext4 -f /drive/partition
        sudo mount -o remount,rw /drive/partition /
 ```       
Replace /drive/partion with the affected drive and partition
