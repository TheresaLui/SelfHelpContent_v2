<properties
	articleId="problemscopingques-netappvolume-crrdelete"
	pageTitle="Issues deleting source or destination volumes"
	description="Issues deleting source or destination volumes"
	authors="b-kiudup"
	ms.author="b-kiudup"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32745368"
	productPesIds="16469"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureNetAppFiles"
/>
# Issues deleting source or destination volumes
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Issues deleting source or destination volumes",
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
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
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
