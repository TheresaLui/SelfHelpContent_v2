<properties
	pageTitle="How to check storage account has not been created and request restore"
	description="How to check storage account has not been created and request restore"
	service="microsoft.storage"
	resource="storageAccounts"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	ownershipId="Centennial_CloudNet_LoadBalancer"
	articleId="54f27767-0879-46e9-bfad-da064cb57ee4"
/>

# How to check storage account has not been created and request restore

1. Validate that the account has not been created.
2. **IMPORTANT** Open Internet Explorer (operation needs silverlight) in **In-Private browsing mode** (Ctrl+Shift+P)
3. Navigate to https://xlocationsn3prod.location-diagnostics.store.core.windows.net
4. Go to Account Summary on the left pane and provide the deleted Storage Account name and select **Search in AccountName** from the drop down.
5. The account lookup **MUST FAIL** with an error like "did not return any results" or the customer has recreated the storage account and you will have to start over.
6. Once we are sure, the account isn’t recreated, we can proceed with requesting a restore
7. Click on the GetDeletedVersions and provide the same storage account name and click on **Get**.
8. You will see the storage account(s) in a new window. Select the storage account with the right CreationTime and DeletionTime as determined from Step 1 above.
9. Click on **Restore Deleted Account**.
10. Upon successful execution the entry will disappear.
11. The details of the storage account should show up. If not, go to **Account Summary** on the left pane and provide the deleted Storage Account name in the top ribbon and select **Search in AccountName** from the drop down once again.
12. Check all details of the storage account and ensure that
13. **Parent Account** should have the correct Subscription ID.
14. **Managed by SRP**? should be **False**
15. Note the Geo Region and Geo Domain. You will use this in future steps.
16. Validate Account Properties
17. Navigate to [Tenant Utils -> Master Commands and choose Get Account Properties](https://xlocationsn3prod.location-diagnostics.store.core.windows.net/master/getaccountproperties.html)
18. Provide the storage account name and hit Get Account Properties
19. If the account is successfully recovered you will see properties listed. If something failed, you will see a blank screen indicating the account isn’t recovered.
20. Also run an nslookup on the account FQDN to confirm DNS entries have been restored.

~~~shell

SET SA={StorageAccountName}
nslookup %SA%.blob.core.windows.net
nslookup %SA%.file.core.windows.net
nslookup %SA%.table.core.windows.net
nslookup %SA%.queue.core.windows.net

~~~
