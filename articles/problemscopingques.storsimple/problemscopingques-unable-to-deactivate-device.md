<properties
	articleId="f7945ba5-bdd2-4909-bfb6-568ccbe2bd7d"
	pageTitle="Scoping unable to deactivate device"
	description="Unable to deactivate device"
	authors="Archana-MSFT"
	ms.author="armukk"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630509"
	productPesIds="15438"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="StorageMediaEdge_AzureStorSimpleSeries"
/>
# Unable to deactivate or delete the device
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Unable to deactivate or delete the device",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "task",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Which device-level task is failing",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Deletion of device",
                    "text": "Deletion of device"
                },
                {
                    "value": "Deactivation of device",
                    "text": "Deactivation of device"
                }
            ],
            "required": false
        },
        {
            "id": "retry",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Have you tried deactivation process again after a few hours?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
