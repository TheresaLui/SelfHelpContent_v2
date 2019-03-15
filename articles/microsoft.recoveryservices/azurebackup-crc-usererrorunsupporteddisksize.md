<properties
	          pageTitle="usererrorunsupporteddisksize"
	          description="usererrorunsupporteddisksize"
		  infoBubbleText="Backup operation was failing due to the disk size limit. See details on the right."
	          service="microsoft.recoveryservices"
	          resource="backup"
	          authors="srinathv"
	          ms.author="srinathv"
		  articleId="azurebackup-crc-usererrorunsupporteddisksize"
	          diagnosticScenario="azurebackup-crc-usererrorunsupporteddisksize"
	          selfHelpType="diagnostics"
	          supportTopicIds="32553276"
	          productPesIds="15207"
	          cloudEnvironments="public"
/>


# UserErrorUnsupportedDiskSize

<!--issueDescription-->
The backup operation failed when backing up VM with disk size greater than 1023GB since your vault is not upgraded to Instant Restore feature. 
<!--/issueDescription-->

## **Recommended Steps**

- Upgrading to Instant Restore will provide support up to 4TB. To avoid failures in the future, upgrade to Instant Restore feature.
- After you upgrade, it will take up to two hours for the subscription to avail this functionality, provide sufficient buffer before you retry the operation. 


## **Recommended Documents**

* Review the [benefits](https://aka.ms/AB-IR-feature-considerations), including the ability to backup disks up to 4TB. 
* Make sure you read the [considerations](https://aka.ms/AB-IR-feature-considerations) section.
* Complete the upgrade following these [instructions](https://aka.ms/AB-IR-upgrade).
