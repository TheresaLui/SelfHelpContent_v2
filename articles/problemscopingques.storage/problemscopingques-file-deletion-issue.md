<properties
	pageTitle="Storage File share or path"
	description="Storage File share or path scoping question"
	authors="Passaree"
    ms.author="passap"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602743"
	productPesIds="16460"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest"
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
            "id": "file_share_or_path",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "File Share or File path",
            "watermarkText": "'FileShare' or 'FileShare/FileName'",
            "required": true,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate start time of the most recent occurrence",
            "required": true,
            "diagnosticInputRequiredClients": "Portal,ASC"
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
