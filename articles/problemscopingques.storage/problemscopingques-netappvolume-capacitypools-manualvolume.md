<properties
	articleId="problemscopingques-netappvolume-flexcapacitypoolsvolume"
	pageTitle="Unable to set or modify throughput level for my volume"
	description="Unable to set or modify throughput level for my volume"
	authors="b-kiudup"
	ms.author="b-kiudup"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32743315"
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
    "title": "Unable to set or modify throughput level for my volume",
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
            "id": "operation",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Operation",
            "watermarkText": "What is the operation that failed",
			"dropdownOptions": [
                {
                    "value": "Create Volume",
                    "text": "Create Volume"
                },
                {
                    "value": "Edit Volume",
                    "text": "Edit Volume"
                },
				{
                    "value": "dont_know_answer",
                    "text": "Don't Know"
                }
			],
            "required": true
        },
		{
            "id": "specific_volume",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Specific to a volume",
            "watermarkText": "Is this specific to one volume or all volumes in this pool?",
			"dropdownOptions": [
                {
                    "value": "Specific Volume",
                    "text": "Specific Volume"
                },
                {
                    "value": "All Volumes",
                    "text": "All Volumes"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Don't Know"
                }
			],
            "required": true
        },
		{
            "id": "sufficient_throughput",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Is there sufficient throughput",
            "watermarkText": "Is there sufficient throughput in the capacity pool?",
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
