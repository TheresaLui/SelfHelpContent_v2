<properties
	articleId="problemscopingques-netappvolume-quota"
	pageTitle="Issue with volume quota"
	description="Issue with volume quota"
	authors="b-kiudup"
	ms.author="b-kiudup"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32784417"
	productPesIds="16469"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureNetAppFiles"
/>
# Issue with volume quota
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Issue with volume quota",
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
            "id": "operation",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Does the issue happen while creating volume or resizing the volume?",
            "watermarkText": "Is issue seen while creating volume or resizing the volume?",
			"dropdownOptions": [
				{
                    "value": "Create",
                    "text": "Create"
                },
                {
                    "value": "Resize",
                    "text": "Resize"
                },
				{
                    "value": "dont_know_answer",
                    "text": "None of the above"
                }
			],
            "required": true
        },
        {
            "id": "problem_description",
            "order": 3,
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
