<properties
	articleId="dc09e316-7077-4d91-9bbf-bfdde2e47cef"
	pageTitle="Scoping for Backups failing or slow"
	description="Backups failing or slow scoping"
	authors="Archana-MSFT"
	ms.author="armukk"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630493"
	productPesIds="15438"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="StorageMediaEdge_AzureStorSimpleSeries"
/>
# Backups are failing or slow
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Backups_failing_or_slow",
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
            "id": "local_backups",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Are the local backup successful?",
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
            "id": "cloud_bandwidth",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Specify the cloud bandwidth available to StorSimple",
            "watermarkText": "Cloud bandwidth in Mbps",
            "required": false
        },
        {
            "id": "dedicated_or_shared",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Is the cloud bandwidth dedicated or shared?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Dedicated",
                    "text": "Dedicated"
                },
                {
                    "value": "Shared",
                    "text": "Shared"
                }
            ],
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 6,
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
