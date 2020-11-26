<properties
	articleId="66e49d4e-1817-4005-b1b3-0ae196883829"
	pageTitle="Scoping recovery operation failed"
	description="Recovery operation failed scoping"
	authors="Archana-MSFT"
	ms.author="armukk"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32630507"
	productPesIds="15438"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	ownershipId="StorageMediaEdge_AzureStorSimpleSeries"
/>
# Recovery operation failed
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Recovery_Operation_failed",
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
            "id": "operation_type",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Which recovery operation is failing?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Clone",
                    "text": "Clone"
                },
                {
                    "value": "Restore",
                    "text": "Restore"
                }
            ],
            "required": false
        },
        {
            "id": "restore_operation",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Is restore from any another backup succeeding?",
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
