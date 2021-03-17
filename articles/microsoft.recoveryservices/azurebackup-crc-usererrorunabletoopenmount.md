<properties
        pageTitle="UserErrorUnableToOpenMount"
        description="UserErrorUnableToOpenMount"
        infoBubbleText="Some mount point is not accessible"
        resource="backup"
        authors="srinathvasireddy"
        ms.author="srinathvasireddy"
        displayOrder=""
        articleId="azurebackup-crc-usererrorunabletoopenmount"
        diagnosticScenario="azurebackup-crc-usererrorunabletoopenmount"
        selfHelpType="diagnostics"
        supportTopicIds=""
        resourceTags=""
        productPesIds="15207"
        cloudEnvironments="public, fairfax, usnat, ussec"
        ownershipId="StorageMediaEdge_Backup"
/>

# Error UserErrorUnableToOpenMount
 
<!--issueDescription-->

We have identified that your backup operation failed because some mount points are either inaccessible or not cleaned up.  
<!--/issueDescription-->

## **Recommended Steps**

To resolve this issue, perform the following:

- Ensure all mount points of fstype Ext3/4, ReiserFS, JFS, XFS are accessible
- After the file recovery option to RESTORE file and folders, if the operation did not cleanup mountpoints and still available on the VM, then the next backup might fail. For more information, refer this [article](https://docs.microsoft.com/azure/backup/backup-azure-restore-files-from-vm#closing-the-connection).
  The filesystem state which is not clean, unmount it by running the command *unmount FilesSystem-name*, ex. *unmount /dev/sdb1*
- After completing the steps retry backup operation

## **Recommended Documents**

- Related error [UserErrorFsFreezeFailed](https://docs.microsoft.com/azure/backup/backup-azure-vms-troubleshoot#usererrorfsfreezefailed---failed-to-freeze-one-or-more-mount-points-of-the-vm-to-take-a-file-system-consistent-snapshot)
- [Application-consistent backup of Azure Linux VMs](https://docs.microsoft.com/azure/backup/backup-azure-linux-app-consistent)

