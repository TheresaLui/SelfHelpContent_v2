<properties
	articleId="1fa746d0-22d2-42bf-a404-95fe2ac4da38"
	pageTitle="Scoping cooling module or battery failure"
	description="Cooling module or battery failure scoping"
	authors="Archana-MSFT"
	ms.author="armukk"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630505"
	productPesIds="15438"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="StorageMediaEdge_AzureStorSimpleSeries"
/>
# Cooling module or battery failure
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "pcm",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "storsimple_devices",
            "order": 1,
            "controlType": "multiselectdropdown",
            "displayLabel": "Device name",
            "watermarkText": "Choose an option",
            "required": false,
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/resourcegroups/{resourcegroup}/providers/Microsoft.StorSimple/managers/{resourceName}/devices?&api-version=2017-06-01",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "name",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Not applicable/No devices available"
                }
            }
        },
        {
            "id": "pcm_slot",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Select the failed or degraded PCM",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "PCM 0",
                    "text": "PCM 0"
                },
                {
                    "value": "PCM 1",
                    "text": "PCM 1"
                }
            ],
            "required": false
        },
        {
            "id": "battery_slot",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Select the PCM in which the battery is failed or degraded",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "PCM 0",
                    "text": "PCM 0"
                },
                {
                    "value": "PCM 1",
                    "text": "PCM 1"
                }
            ],
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 5,
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
