<properties
	articleId="problemscopingques-netappvolume-crrbreak"
	pageTitle="Issues breaking a replication relationship"
	description="Issues breaking a replication relationship"
	authors="b-kiudup"
	ms.author="b-kiudup"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32745367"
	productPesIds="16469"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureNetAppFiles"
/>
# Issues breaking a replication relationship
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Issues breaking a replication relationship",
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
            "id": "relationship_broken",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Was the relationship broken successfully",
            "watermarkText": "Was the relationship broken successfully",
			"dropdownOptions": [
				{
                    "value": "Mirrored",
                    "text": "Mirrored"
                },
                {
                    "value": "Uninitialized",
                    "text": "Uninitialized"
                },
				{
                    "value": "Idle",
                    "text": "Idle"
                },
				{
                    "value": "Transferring",
                    "text": "Transferring"
                },
				{
                    "value": "dont_know_answer",
                    "text": "I do not know"
                }
			],
            "required": true
        },
		{
            "id": "source_volume_name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Source Volume Name",
            "watermarkText": "Source Volume Name",
            "required": false
        },
		{
            "id": "destination_volume_name",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Destination Volume Name",
            "watermarkText": "Destination Volume Name",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 5,
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
