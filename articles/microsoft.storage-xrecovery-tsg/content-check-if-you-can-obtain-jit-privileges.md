<properties
	pageTitle="How to check if you can obtain JIT privileges"
	description="How to check if you can obtain JIT privileges"
	service="microsoft.storage"
	resource="storageAccounts"
	authors="symondsk"
	ms.author="ksymonds"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	ownershipId="StorageMediaEdge_AccountManagement"
	articleId="9f5179df-377a-447a-a0af-ab921063a79a"
/>

# How to check if you can obtain JIT privileges

1. Create an IcM using this [JIT ICM Template ](https://portal.microsofticm.com/imp/v3/incidents/create?tmpl=74a1g3) (Must use this link to avoid confusion)
2. This will be used in multiple steps and start by obtaining JIT permissions to check and trigger a classic storage account restore. **NOTE:** If you are not a member of TM-CSSStgRec group, you will need to stop here and reach out to a TA who has access.
3. Navigate to JIT access portal : https://jitaccess.security.core.windows.net/WorkFlowTempAccess.aspx
	1. WorkItem: **ICM number as created using template link** [JIT ICM Template ](https://portal.microsofticm.com/imp/v3/incidents/create?tmpl=74a1g3) (Must use this link to avoid confusion)
	2. Justification: **Classic Storage account recovery**
	3. Resource Type: **XDS**
	4. Tenant: **xlocationsn3prod** (case sensitive)(NOT THE STORAGE TENANT)
	5. Access: **Storage-CSSRole**
4. After filling in all the fields, click on **Validate and Add Resource** button followed by Submit.
5. Once the request is submitted, click on **Apply/Refresh**
6. If the output looks like the below image, then the permission has been successfully auto granted. If not you will have to wait for someone to approve the access.

## Recommended Documents

1. [JIT ICM Template ](https://portal.microsofticm.com/imp/v3/incidents/create?tmpl=74a1g3)
