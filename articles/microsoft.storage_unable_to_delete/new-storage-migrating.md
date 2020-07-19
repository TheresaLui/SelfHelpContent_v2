<properties
	pageTitle="Storage account is in the process of migrating"
	description="Storage account is in the process of migrating"
	service="microsoft.storage"
	resource="storageAccounts"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds="32602738"
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public, fairfax, usnat, ussec"
	articleId="5a2a90e9-4bfc-4e4b-9077-b1c71ceb042d"
	ownershipId="Centennial_CloudNet_LoadBalancer"
/>

# Storage account is in the process of migrating

1. This error usually occurs when a customer started a migration from Classic to ARM and did not perform the commit operation.
2. In this specific cases, an ASM to ARM migration seems to be in progress for the customer's Storage Account. Follow the next steps to unblock the customer to being able to delete the desired Storage Account.
    1. First, customer can perform a Commit operation for the migration process to be completed:

~~~powershell

Move-AzureStorageAccount-Commit -StorageAccountName storageAccountName -Debug

~~~
   3. If the Commit operation failed for any reason they can also Abort the migration by executing the command:

~~~powershell

Move-AzureStorageAccount-Abort -StorageAccountName storageAccountName -Debug

~~~

**Review Migration related operations executed(Validate/Prepare/Commit)** 

1. Get/Open [Kusto.Explorer](http://kusto/ke/Kusto.Explorer.application). More information at [Tools reference](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD?wikiVersion=GBmaster&pagePath=%2fGeneralPages%2fAzure%2fAzure_Virtual%20Machine_Tools%20reference).
2. Open a New Query Tab and Select the Armprod>ARMProd Connection.
2. Fill the following [example query](https://armprod.kusto.windows.net/ARMProd?query=H4sIAAAAAAAEAH1UXW%2FaMBR9R%2bI%2FuHmiUryYhM9qrcRoSqPxpSRo6qPjXMAb%2bZjttFvVHz8Hxgg03Vtkn3vOucc391Gp3EtZlvB048PPAqSS6A29bEEAkkUkmeC54lnqxej2FhntnsM6DmXY6dMO7jjdDh4M7D4eAunbcXtNCdgGQs2GZR1ZFBUbUCvBEctSRXkqkWEFKhN0AyPGsiJV0jIsC9E0RrXoXS5jlkGcMSVoKtcgtIRllfgsB0FLf3OaQKUkpJsNxHvYgbcOfnXCT70g%2FOo%2bBbqixNW5kOeWNbIkL%2bHNxrHXrY5zBmqbxehKpzVxQ6NWGdJYvnC1RcZouZx641HoLeaTUeh%2bGz0F1rGmzoVOgP3AhZSM4OcUFCakjWX0C0sV7fb9vlXDLw0FiqpCjrMY0B2yCTnZrRNYZ0IVKay53Co9De%2b9VFKbeWN%2FESwewk%2FePPAmj2FgzdzQ98b37oM398qmguPL1mkluN2NO6zXJf2103Fs6DlORMi6PrTa56o2ew4vx%2FXenbqhawWrL8HY95Z7Q5bvBouVP3Yn%2FmK1%2FH%2Fa99PZxTTrXyXR6H8KPmy4VCDw6LUQ4CdLkT3zGMQD6NAFGKewP5qAGd8czo2qzlIA4xJCnoB%2bvyRHd7copgqUPmgZNmkPMXGw3UeE3BBiXO8zflf0%2bYMi27npDo3rk7k6uTR7aeEhifewXGTfgan3QPOiMbP6E5iXA2ieYjZ1lkLAjh7Wi1mN1rLMy%2b1jFhLEaAOpQuUt23H96eWjOBYgpYkE6L0AQisEWSEYlDQyp0xz6TMqkgDEM2fwd8tpxuPDykLrCv4KKPpdtXdhfdhxBoNuZGM27DHc6fcIpnrt4fVwGEW23ov9boSiH3m8YwhVWff7onWNSvrzpvaNlLfZunV%2bY14fvO14whXqNhvNxh8fxPWsqwUAAA%3d%3d&web=0) with your environment details to get further information.

~~~kusto

    HttpIncomingRequests | where subscriptionId == "<SubscriptionId>"  | where httpMethod != "GET"| where targetUri contains "<StorageAccountName>" | where operationName endswith "Migration"| where PreciseTimeStamp >= now(-90d)| project PreciseTimeStamp , operationName , httpMethod , httpStatusCode , targetUri, correlationId, commandName

~~~



**Recommended Documents**

1. [Storage Account in process of migrating](https://supportability.visualstudio.com/AzureVMPOD/_wiki/wikis/AzureVMPOD/265688/Azure_Storage_TSG_Storage-account-is-in-the-process-of-being-migrated-and-hence-cannot-be-changed)
