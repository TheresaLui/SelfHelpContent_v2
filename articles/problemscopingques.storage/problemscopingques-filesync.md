<properties
	pageTitle="Storage File Sync"
	description="Storage File Sync scoping question"
	authors="kartikshah9"
    ms.author="kashah"
	articleId="StorageScoping_file_sync"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32675720,32675721,32675722,32675723,32675724,32675725,32675726"
	productPesIds="16460"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	ownershipId="StorageMediaEdge_StorageFiles"
/>
# Storage File Sync scoping question
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Storage File Sync scoping question",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "file_sync",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "File Sync resource",
            "watermarkText": "Choose a File Sync",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/providers/Microsoft.StorageSync/storageSyncServices?api-version=2018-04-02",
                "jTokenPath": "value",
                "textProperty": "id",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            },
            "DropdownOptions": [
                {
                    "value": "NoFileSync",
                    "text": "Not specific to a File Sync"
                }
            ],
            "required": true
        },
        {
            "id": "syncgroup",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Sync Group Name",
            "watermarkText": "Enter Sync Group Name else enter Not Applicable",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "watermarkText": "If applicable, please provide sync group name, server endpoint name, cloud endppoint and error message.",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
