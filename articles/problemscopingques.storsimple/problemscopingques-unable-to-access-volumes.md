<properties
	articleId="48349c76-e647-4d80-bc25-ecc5c5e96c61"
	pageTitle="Scoping unable to access volumes"
	description="Unable to access volumes scoping"
	authors="Archana-MSFT"
	ms.author="armukk"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630508"
	productPesIds="15438"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="StorageMediaEdge_AzureStorSimpleSeries"
/>
# Unable to access volumes
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Unable to access volumes",
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
            "id": "vol_names",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Name the volumes (if specific volumes) that are inaccessible",
            "watermarkText": "Names of inaccessible volumes",
            "required": false
        },
        {
            "id": "mount",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Have you tried to mount the volumes on another server?",
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
            "id": "initiator_property",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Do iSCSI initiator properties show the target in connected state?",
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
            "id": "changes_updates",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Were there any changes/updates made on the server/network?",
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
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 7,
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
