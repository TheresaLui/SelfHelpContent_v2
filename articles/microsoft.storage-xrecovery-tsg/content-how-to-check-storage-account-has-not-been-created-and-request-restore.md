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

### Obtain JIT Privileges

1. Create an IcM using this [JIT ICM Template ](https://icm.ad.msft.net/imp/v3/incidents/create?tmpl=74a1g3) (Must use this link to avoid confusion)
2. This will be used in multiple steps and start by obtaining JIT permissions to check and trigger a classic storage account restore. **NOTE:** If you are not a member of TM-CSSStgRec group, you will need to stop here and reach out to a TA who has access.
3. Navigate to JIT access portal : https://jitaccess.security.core.windows.net/WorkFlowTempAccess.aspx
	1. WorkItem: **ICM number as created using template link** [JIT ICM Template ](https://icm.ad.msft.net/imp/v3/incidents/create?tmpl=74a1g3) (Must use this link to avoid confusion)
	2. Justification: **Classic Storage account recovery**
	3. Resource Type: **XDS**
	4. Tenant: **xlocationsn3prod** (case sensitive)(NOT THE STORAGE TENANT)
	5. Access: **Storage-CSSRole**
4. After filling in all the fields, click on **Validate and Add Resource** button followed by Submit.
5. Once the request is submitted, click on **Apply/Refresh**
6. If the output looks like the below image, then the permission has been successfully auto granted. If not you will have to wait for someone to approve the access.

## Recommended Documents

1. [JIT ICM Template ](https://icm.ad.msft.net/imp/v3/incidents/create?tmpl=74a1g3)

### Request Restore

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
