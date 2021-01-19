<properties
	pageTitle="NetworkSourrceDeleted Scenario"
	description="NetworkSourrceDeleted Scenario"
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
	articleId="6ac5e90c-696b-444c-b525-4fabd9b37cd6"
   	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# NetworkSourrceDeleted Scenario

## Overview
The NetworkSourceDelete error usually happens when a Firewall ACL had been created with a Subnet that was deleted afterwards. You may experience this error when a Subnet with the same name as the previosuly deleted one is recreated and you attempt to add it as a new Firewall ACL in other Storage Account.

## Review customer failed operation 
1. You may ommmit this section if you already have the error message provided by the customer. Otherwise continue to retrieve those details:
2. Choose one of the following methods:
    1. **Azure Support Center(ASC)**
        1. Navigate to the Storage Account affected within ASC Resource Explorer.
        2. Open the ***Operations*** tab.
        3. Perform a query using the SRP Operations, filter for the appropriate timeframe.
        4. Review ***Failed*** operations with error code ***NetworkAclsNetworkSourceDeleted***
    2. **Kusto**
        1. Using the folllowing kusto. Make sure to modify the Storage Account name and adjust the timeframe. [Query example link](https://armprod.kusto.windows.net/ARMProd?query=H4sIAAAAAAAEAH2RTU%2fCQBCG7yT8h7EXSkJoRTlA1KQBDo2CxNaDMR6W3ZGutl0yOw2a%2bONdCkSUyG3nnffZ%2bZJ5ZRnJb0VUrMioVrurBIuFsOi0h%2bl8qyWZwYX5mJRMGi18wTpDQiC0piKJsYJMWPCC4tOyIbFEIaWpSvZAlArANyskwdqUM1Hg1jvVkow1r9xNtogHhuCkcZQLa7Xc%2b9v157%2bJsxq5i5P0dvKUeP86osdxnAbRKI3vZx4ANBtBsJ9qTii1xVQXmLAoVnBzDW4pyE7wvX4wCHphL4QwHIbhrokj5OoYOR9A72LYH9RUs3Gqmlgav3eZHbjcbdwUvFl%2b3f8MeW3oPZK53T2T%2bhJjzJFReRvSMW8o%2bbhC5%2fBwnT%2f7qZNVzoleloIr2ig%2f1TsgDRHmtT9WLhR5jhSvIqUc5%2fLPLa2wZM2frZdvWsMF%2fl4CAAA%3d&web=0).

~~~powershell

cluster('Armprod').database('ARMProd').ShoeboxEntries | where resourceId has "/mystorageaccount" and  (operationName has "Microsoft.Storage" or operationName has "Microsoft.ClassicStorage") and operationName !has "LISTKEYS" and operationName !has "AUDIT/ACTION"   
//| where PreciseTimeStamp >= datetime("5/9/2020 00:00") and PreciseTimeStamp <= datetime("5/9/2019 23:59:00")
| where PreciseTimeStamp >= ago(24h)
| where properties has "NetworkAclsNetworkSourceDeleted"
| project PreciseTimeStamp , resourceId , operationName , resultSignature , properties, correlationId, callerIpAddress, ['identity']

~~~

2. Look at the error message details within the **properties** column.
3. Regardless of the method used above, check the error message, note all the ***Storage Accounts*** where the ***VNET Subnet*** is located.

## Check status of the Storage Account ACLs

5. Choose one of the following methods:
    1. **Azure Support Center(ASC)**
        1. Navigate to the Storage Account affected within ASC Resource Explorer.
       2. Within the ***Summary*** tab, search the ***Firewalls and Virtual Networks*** subsection
       3. Review the ACLs in this section and pay attention to the value of the **State** property for each subnet.
    2. **Jarvis Actions**
        1. Open Jarvis Actions.
        2. Select SRP --> SRP Operations --> **Get RSRP Subscription Details**. [Query example link](https://jarvis-west.dc.ad.msft.net/B27EC1ED?genevatraceguid=f2c08e42-fa9a-42db-8ab7-26ce29aa7516).
        3. Adjust the query with the correct ***SubscriptionId*** and ***Region*** where the ***Storage Account*** being investigated is present and execute the query.
        4. Find the affected ***Storage Account/s*** and look at the properties under properties > networkAcls > **virtualNetworkRules**
        5. Review the ACLs in this section and pay attention to the value of the **State** property for each subnet.
6. If there are one or more Subnets with NetworkSourceDeleted, you have confirmed that the cusotmer is experiencing this scenario. Otherwise, the customer is not experiencing this scenario.

If this did not solve your issue, please restart the troubleshooter and choose the Generic Issues Troubleshooting option.
