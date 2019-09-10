<properties
	pageTitle="Storage migration using AzCopy"
	description="Issues migrating data using AzCopy"
	authors="Sijia"
        ms.author="siz"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630513"
	productPesIds="16460"
	cloudEnvironments="public,MoonCake,FairFax"
	schemaVersion="1"
	articleId="8f19bac0-2ee7-4d75-9ba6-51913ba46fc4"
/>

# Files migration with AzCopy
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Issues migrating data using AzCopy",
    "fileAttachmentHint": "Upload AzCopy Log for fast case resolution. Log files are located in the %USERPROFILE\\\\.azcopy directory on Windows, or in the $HOME\\\\.azcopy",
    "diagnosticCard": {
        "title": "What caused AzCopy issue?",
        "description": "Our Data Migration AzCopy troubleshooter can help you troubleshoot and solve your problem.",
        "insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource. Please ensure the information provided is accurate and in the approved format. Also, see our manual troubleshooting steps below to troubleshoot your problem."
    },
    "formElements": [
          {
            "id": "storage_account_from",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Source storage account",
            "watermarkText": "Select storage account",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionId}/providers/Microsoft.Storage/storageAccounts?api-version=2018-07-01",
                "jTokenPath": "value",
                "textProperty": "id",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "From a different subscription, external source or not applicable"
                }
            },
            "required": true,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
	 {
            "id": "storage_account_to",
            "visibility": "true",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Destination storage account",
            "watermarkText": "Enter storage account name",
            "required": true,
            "diagnosticInputRequiredClients": "Portal,ASC"
          }
    ],
    "$schema": "SelfHelpContent"
}
---
