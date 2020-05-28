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
    cloudEnvironments="public, blackForest, fairfax, mooncake, usnat, ussec"
	ownershipId="AzureData_HDInsight"
/>

# We ran diagnostics on your resource and found the following issue
<!--issueDescription-->
The virtual machine booted up with a read-only file system. The following node(s) are in read-only mode: <!--$AlertHost-->[AlertHost]<!--/$AlertHost--> <br>

The drive has to be remounted in read-write mode.
<!--/issueDescription-->

## **Recommended Steps**

1. You can connect to Ambari service using Secure Shell (SSH): `ssh <clustername>-ssh.azurehdinsight.net`

2. SSH into the affected node and run the following command to identify the read-only disk with drive and partition: `mount -l | grep sd`

3. Run the following commands to change it to read-write mode:

 ```       
        sudo fsck.ext4 -f /drive/partition
        sudo mount -o remount,rw /drive/partition
 ```
 
    Replace /drive/partition with the affected drive and partition e.g /dev/sda
