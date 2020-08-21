<properties
	articleId="problemscopingques-netappvolume-crrunhealthy"
	pageTitle="Replication relationship is showing as unhelathy or not available"
	description="Replication relationship is showing as unhelathy or not available"
	authors="b-kiudup"
	ms.author="b-kiudup"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32745372"
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
    "title": "Replication relationship is showing as unhelathy or not available",
    "fileAttachmentHint": "",
    "formElements": [
		{
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
		{
            "id": "authorized",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Was the relationship authorized within 1 hour",
            "watermarkText": "Was the relationship authorized on source volume side within 1 Hour of DP volume creation",
			"dropdownOptions": [
				{
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
				{
                    "value": "dont_know_answer",
                    "text": "I do not know"
                }
			],
            "required": true
        },
		{
            "id": "operation",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Operation after which this issue is seen",
            "watermarkText": "Operation after which this issue is seen",
            "required": true
        },
		{
            "id": "source_volume_name",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Source Volume Name",
            "watermarkText": "Source Volume Name",
            "required": false
        },
		{
            "id": "destination_volume_name",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Destination Volume Name",
            "watermarkText": "Destination Volume Name",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 6,
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
