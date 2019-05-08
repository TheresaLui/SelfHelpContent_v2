<properties
pageTitle="3rd party service issues when Storage Firewalls is enabled"
description="Firewall is not compatible with certain Storage operations"
infoBubbleText="See details on the right"
service="microsoft.storage"
resource="storage"
authors="passaree"
displayOrder=""
articleId="Storagev2insights_acc_firewall_addIP"
diagnosticScenario="Storage issues when Storage Firewalls is enabled"
selfHelpType="diagnostics"
supportTopicIds=""
productPesIds=""
cloudEnvironments="public"
/>

# Third-party services issues when Storage Firewalls is enabled

<!--issueDescription-->
We have detected that [Storage Firewalls and Virtual Networks](https://docs.microsoft.com/azure/storage/common/storage-network-security) is configured on the Storage Account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->**. Third-party services running outside Azure must ensure that their IPs are in the allowed list when Storage Firewalls and Virtual Networks is configured.<br> 

Only the following IPs are allowed to access Storage Account **<!--$ResourceName-->[ResourceName]<!--/$ResourceName-->**:
<!--$IPRules-->[IPRules]<!--/$IPRules-->

Please check if the client IP is in the allowed IP ranges that are authorized to access this Storage Account. You can [grant access to the associated IP ranges](https://docs.microsoft.com/azure/storage/common/storage-network-security#grant-access-from-an-internet-ip-range) to ensure that your application IP is in the allowed list.

<!--/issueDescription-->