<properties
	articleId="problemscopingques-netappvolume-flexcapacitypools"
	pageTitle="Unable to create a Manual Capacity pool"
	description="Unable to create a Manual Capacity pool"
	authors="b-kiudup"
	ms.author="b-kiudup"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32743313"
	productPesIds="16469"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureNetAppFiles"
/>
# Unable to create a Manual Capacity pool
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Unable to create a Manual Capacity pool",
    "fileAttachmentHint": "",
    "formElements":[
		{
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
		{
            "id": "pool_name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Pool Name",
            "watermarkText": "Pool name of failed capacity pool",
            "required": true
        },
		{
            "id": "pool_count",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Number of Pools in the account",
            "watermarkText": "Number of pools in the NetApp account",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
