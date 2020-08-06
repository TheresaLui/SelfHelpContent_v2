<properties
	pageTitle="Storage File connectivity or performance issue"
	description="Storage File connectivity or performance scoping question"
	authors="Passaree"
    ms.author="passap"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602761,32602762"
	productPesIds="16460"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	articleId="f55638b4-3688-4399-a0f6-dd6ef04717c9"
	ownershipId="StorageMediaEdge_StorageFiles"
/>
# Storage File connectivity or performance issue
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Storage File connectivity or performance scoping question",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "What caused my Azure Files connectivity issue?",
        "description": "Our Azure Files connectivity troubleshooter can help you troubleshoot and solve your problem.",
        "insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource. Please ensure that File Share or File Path provided is in the approved format. Also, see our manual troubleshooting steps below to troubleshoot your problem."
    },
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate start time of the most recent occurrence",
            "required": true,
            "diagnosticInputRequiredClients": "ASC"
        },
        {
            "id": "file_share_or_path",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "File Share or File path",
            "watermarkText": "'FileShare' or 'FileShare/FileName'",
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
