<properties
	articleId="problemscopingques-netappvolume-flexcapacitypoolsconvert"
	pageTitle="Unable to convert an Auto QoS Capacity Pool to Manual"
	description="Unable to convert an Auto QoS Capacity Pool to Manual"
	authors="b-kiudup"
	ms.author="b-kiudup"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32743314"
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
    "title": "Unable to convert an Auto QoS Capacity Pool to Manual",
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
            "id": "service_level_dropdown",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Service Level",
            "watermarkText": "Service Level of the pool",
            "dropdownOptions":[
                {
                    "value": "Standard",
                    "text": "Standard"
                },
                {
                    "value": "Premium",
                    "text": "Premium"
                },
                {
                    "value": "Ultra",
                    "text": "Ultra"
                },
				{
				    "value":"dont_know_answer",
					"text":"Dont Know"
				}
			],
			"required": true
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
