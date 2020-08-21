<properties
        pageTitle="GuestAgentCertificateNotFound"
        description="guestagentcertificatenotfound"
        infoBubbleText="Virtual machine guest agent certificate not found"
        resource="backup"
        authors="srinathvasireddy"
        ms.author="srinathvasireddy"
        displayOrder=""
        articleId="azurebackup-crc-guestagentcertificatenotfound"
        diagnosticScenario="azurebackup-crc-guestagentcertificatenotfound"
        selfHelpType="diagnostics"
        supportTopicIds=""
        resourceTags=""
        productPesIds="15207"
        cloudEnvironments="public, fairfax, usnat, ussec"
        ownershipId="StorageMediaEdge_Backup"
/>

 

# Error GuestAgentCertificateNotFound

 
<!--issueDescription-->

We have identified that your backup operation failed because the VM does not have a valid guest agent certificate.<br>
The certificates are built by the Azure fabric controller and passed to the VM Agent. If you stop and start the VM every day, a new certificate might be created by the fabric controller. The certificate is stored in the computer's Personal certificates store. These certificates can be deleted, the VM Agent re-creates certificates if needed
 
<!--/issueDescription-->



## **Recommended Steps**

To resolve this issue, perform the following:

- [Ensure System time is not out of sync](https://docs.microsoft.com/azure/virtual-machines/windows/time-sync).
- Check CRP certificate status<br>
  Launch console with windows+R > type 'MMC.exe' > Go to 'File Menu' > Add/Remove Snap-in <br>
  Select the Certificates snap-in for Computer Account > Choose Local Account > Go to Personal Certificate Repo <br>
  
  Please verify if CRP certificate is expired. If yes, then deallocate and start VM again from the Portal. There is a known issue with CRP certificate and reboot should fix same.

## **Recommended Documents**

- Know more, [Virtual machine extensions and features for Windows](https://docs.microsoft.com/azure/virtual-machines/extensions/features-windows )
