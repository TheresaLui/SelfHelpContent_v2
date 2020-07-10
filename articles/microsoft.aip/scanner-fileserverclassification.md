<properties
	pageTitle="Azure Information Protection - Scanner - File Server Classification Issues"
	description="Azure Information Protection - Scanner - File Server Classification Issues"
	service="microsoft.aip"
	resource="aip"
	authors="orbarak-ms"
	ms.author="orbarak"
	articleId="Scanner_FileServerClassification"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32629558"
	resourceTags=""
	productPesIds="14997"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	ownershipId="AzureIdentity_InformationProtection"
/>

# Azure Information Protection - Scanner

## **Recommended Steps**

1. Make sure your [policies are set](https://docs.microsoft.com/azure/information-protection/configure-policy) to automatic labeling or have a default label in the policy
2. Open the relevant document in Office and verify if the intended label is being applied
3. Make sure that the relevant file type is configured for label/protection as described here: [File types supported by the Azure Information Protection client](https://docs.microsoft.com/azure/information-protection/rms-client/client-admin-guide-file-types#supported-file-types-for-classification-and-protection). In addition, if you want to change the default behavior, follow this guidelines: [Changing the default protection level of files](https://docs.microsoft.com/azure/information-protection/rms-client/client-admin-guide-file-types#changing-the-default-protection-level-of-files)
4. Review [Files that cannot be protected by default](https://docs.microsoft.com/azure/information-protection/rms-client/client-admin-guide-file-types#files-that-cannot-be-protected-by-default) and [Limitations for container files, such as .zip files](https://docs.microsoft.com/azure/information-protection/rms-client/client-admin-guide-file-types#limitations-for-container-files-such-as-zip-files)
5. If you're still experiencing the issue, collect Azure Information Protection scanner logs and attach the exported logs to a support ticket

### Export Azure Information Protection Scanner logs

1. Navigate to `%localappdata%\Microsoft\MSIP` under the user context running the scanner service
2. Zip all the contents under the MSIP folder
3. Save the logs to your choice of location, and attach them to your service request

## **Recommended Documents**

* [Deploying the Azure Information Protection scanner to automatically classify and protect files](https://docs.microsoft.com/azure/information-protection/deploy-aip-scanner)<br>
* [Review Azure Information Protection documentation](https://docs.microsoft.com/azure/information-protection/what-is-information-protection)<br>
* [Requirements for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/requirements)<br>
* [Download Azure Information Protection client](https://www.microsoft.com/download/details.aspx?id=53018)
