<properties
	pageTitle="Storage File share or path"
	description="Storage File share or path scoping question"
	authors="Passaree"
    ms.author="passap"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602758"
	productPesIds="16460"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	articleId="9d8052f8-c738-48ca-940d-c4ddaf89ba30"
	ownershipId="StorageMediaEdge_StorageFiles"
/>
# Storage File share or path scoping question
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Storage File share or path scoping question",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "file_share_or_path",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "File Share or File path",
            "watermarkText": "'FileShare' or 'FileShare/FileName'",
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate start time of the most recent occurrence",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---