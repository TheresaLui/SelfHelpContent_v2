<properties
	articleId="problemscopingques-netappvolume-volumedeletion"
	pageTitle="Unable delete a NetApp volume"
	description="NetApp volumes deletion questions"
	authors="b-amkohl"
	ms.author="b-amkohl"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32740770"
	productPesIds="16469"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest"
	schemaVersion="1"
	ownershipId="AzureNetAppFiles"
/>
# NetApp volume deletion issue
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Unable to delete a NetApp volume",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "snapshot",
            "visibility": "null",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Does the volume have a snapshot?",
            "watermarkText": "Choose if the volume has a snapshot",
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
                    "text": "Other or none of the above",
                    "value": "dont_know_answer"
                }
            ],
            "required": true
        },
        {
            "id": "Volume",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Provide the name of the Volume",
            "watermarkText": "Filter by name",
            "dynamicDropdownOptions": {
                "dependsOn": "resourceGroup",
                "uri": "{resourceId}?api-version=2018-06-01",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
		"valuePropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other or none of the above"
                }
            },
            "DropdownOptions": [
                {
                    "value": "Unable to retrieve list of VMs",
                    "text": "Unable to retrieve list of VMs"
                }
            ],
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 100,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 1000,
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
