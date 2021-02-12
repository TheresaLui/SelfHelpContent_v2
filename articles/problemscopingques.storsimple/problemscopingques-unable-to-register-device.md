<properties
	articleId="7281bab8-cc67-4e8b-8b8a-643f98134169"
	pageTitle="Scoping unable to register device"
	description="Unable to register device"
	authors="Archana-MSFT"
	ms.author="armukk"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630510"
	productPesIds="15438"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="StorageMediaEdge_AzureStorSimpleSeries"
/>
# Unable to register device
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Unable to register device",
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
            "id": "data_ports",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Is port 9354, 443 & 80 open on all Data0 IPs?",
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
            "id": "encryption_key",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Is a valid service data encryption key being used for registration?",
            "watermarkText": "Choose an option",
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
                    "value": "Not sure",
                    "text": "Not sure"
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
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Include output."
                },
                {
                    "text": "Run `invoke-hcsdiagnostics -scope network` and provide output below to assist in troubleshooting the issue."
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
