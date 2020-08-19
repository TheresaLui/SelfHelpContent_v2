<properties
	articleId="problemscopingques-netappvolume-crrresync"
	pageTitle="Issues during resync"
	description="Issues during resync"
	authors="b-kiudup"
	ms.author="b-kiudup"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32745369"
	productPesIds="16469"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureNetAppFiles"
/>
# Issues during resync
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Issues during resync",
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
            "id": "resync_direction",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "In which direction was resync done",
            "watermarkText": "In which direction was resync done",
			"dropdownOptions": [
				{
                    "value": "Source to Destination",
                    "text": "Source to Destination"
                },
                {
                    "value": "Destination to Source",
                    "text": "Destination to Source"
                },
				{
                    "value": "dont_know_answer",
                    "text": "Don't Know"
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
