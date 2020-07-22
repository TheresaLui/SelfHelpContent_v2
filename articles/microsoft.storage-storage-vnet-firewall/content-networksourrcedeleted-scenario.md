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
        1. Using the folllowing kusto. Make sure to modify the Storage Account name and adjust the timeframe. [Query example link](https://armprod.kusto.windows.net/ARMProd?query=H4sIAAAAAAAEAH2RTU%2fCQBCG7036H8ZewITYWuUAUZMGODQqmrQejPGw7o50te02s9MgiT%2betkBEidx2Zt5n3%2flIMoNv5mtWMmm08A3LDAmB0JqaJMYKMmHB84uVZUNigUJKU5fsgSgV9E2FJFibci4K3EjvtSRjzTufJRvCA0NwVDjJhbVa7vSn3d%2b%2fiZMOuYuT9Hb2nHj%2fKqKnaZz60SSNH%2bYeALiO7%2b%2bGeiSU2mKqC0xYFBXcXIMSjNwk%2bt7QH%2flhEAYQBOMg2DZxgFwdIucjCC%2fGw1FHuc4xN7Ew%2ffAy21NV1E7B7e67%2fufIS0Ofkczt9pl0h5hijozKa8mG%2bUDJhw6D%2fbsN%2fuynK9Y5J3pRCq6pzfy4D0AaIsw7fayaUOQ5UlxFSjVcU3%2fpaYUla171Xl3Hddaaow0kOgIAAA%3d%3d&web=0).

~~~powershell
ShoeboxEntries | where resourceId has "/mystorageaccount" and (operationName has "Microsoft.Storage" or operationName has "Microsoft.ClassicStorage") and operationName !has "LISTKEYS" and operationName !has "AUDIT/ACTION"   
//| where PreciseTimeStamp >= datetime("5/9/2020 00:00") and PreciseTimeStamp <= datetime("5/9/2019 23:59:00")
| where PreciseTimeStamp >= ago(24h)
| where properties has "NetworkAclsNetworkSourceDeleted"
| project PreciseTimeStamp , resourceId , operationName , resultSignature , properties, correlationId, callerIpAddress, ['identity']
~~~
       2. Look the error message details within the ***properties*** column.


4. Regardless of the method used above, check the error message, note all the ***Storage Accounts*** where the ***VNET Subnet*** is located.
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
7. Answer the question below appropriately.
