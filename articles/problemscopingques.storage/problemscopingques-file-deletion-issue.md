<properties
	pageTitle="Storage File share or path"
	description="Storage File share or path scoping question"
	authors="Passaree"
    ms.author="passap"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32736816"
	productPesIds="16460"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	articleId="fbd7391e-423c-468a-9716-a536279a3d3a"
	ownershipId="StorageMediaEdge_StorageFiles"
/>
# Storage File share or path scoping question
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Storage File share or path scoping question",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "What caused my Azure Files deletion issue?",
        "description": "Our Azure Files deletion troubleshooter can help you troubleshoot and solve your problem.",
        "insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource. Please ensure that File Share or File Path provided is in the approved format. Also, see our manual troubleshooting steps below to troubleshoot your problem."
    },
    "formElements": [
        {
            "id": "file_share",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "File share",
            "watermarkText": "Select File share",
            "dynamicDropdownOptions":
            {
                "uri": "/subscriptions/{subscriptionid}/resourceGroups/{resourcegroup}/providers/Microsoft.Storage/storageAccounts/{resourcename}/fileServices/default/shares?api-version=2019-06-01",
                "jTokenPath": "value",
                "textProperty": "name",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions":
                {
                    "value": "dont_know_answer",
                    "text": "None of the above"
                },
                "dropdownOptions":[
                    {
                        "value": "NoFileShare",
                        "text": "NA"
                    }
                ]
            }
            "required": false,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "file_share_or_path",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "File path",
            "watermarkText": "Please enter full path for file that cannot be deleted - FileShare/Folder/FileName",
            "required": true,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate start time of the most recent occurrence",
            "required": true,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
