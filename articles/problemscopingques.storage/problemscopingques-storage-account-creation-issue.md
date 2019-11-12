<properties
	pageTitle="Storage Account creation issues"
	description="Issues creating storage account scoping question"
	authors="Passaree"
    ms.author="passap"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32639215,32602693,32639216,32639217,32639218,32639219,32639220,32639214"
	productPesIds="15629"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest"
	schemaVersion="1"
	articleId="08df64c4-7e4e-4ebc-9012-31a0dd43a37e"
/>
# Issues creating Storage Account
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Storage account creation issue",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "storage_account_name",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Name of storage account that failed to create",
            "required": false
        },
        {
            "id": "correlation_id",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Correlation ID of the failed event",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate time when account creation failed",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---