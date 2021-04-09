<properties
	pageTitle="Storage account failover"
	description="Issue with storage account failover"
	authors="Lea"
    ms.author="leakkari"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32631234"
	productPesIds="15629"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	articleId="9BD48974-4A51-4A44-A68C-9BB5E9D8F148"
	ownershipId="StorageMediaEdge_AccountManagement"
/>
# Storage account failover
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Issue with storage account failover",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Issue with storage account failover",
        "description": "This troubleshooter can help resolve issues related to storage account failover. Submit your issue to determine the best possible solution",
        "insightNotAvailableText": "Our troubleshooter did not identify remediation for your issue. See the recommended documentation link to troubleshoot your issue"
    },
    "formElements": [
        {
			"id": "storage_account_name",
			"order": 1,
            "visibility":"service_type == account",
			"controlType": "textbox",
			"displayLabel": "Name of the storage account with failover issue",
            "watermarkText":"StorageAccountName1; StorageAccountName2; StorageAccountName3 ",
			"required": true,
			"diagnosticInputRequiredClients": "Portal,ASC"
		},
        {
            "id": "error_message",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Error message received",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": true,
            "useAsAdditionalDetails": true,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true,
            "diagnosticInputRequiredClients": "Portal,ASC"
        }
    ],
    "$schema": "SelfHelpContent"
}
---
