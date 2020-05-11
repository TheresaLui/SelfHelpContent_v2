<properties
	pageTitle="Blob Lifecycle Management scoping questions"
	description="Blob Lifecycle Management scoping questions"
	authors="annayak"
    ms.author="annayak"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32683730,32691063"
	productPesIds="16459,16598"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	articleId="StorageScoping_Blob_Lifecycle_Management"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>
# Blob Lifecycle Management
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Blob Lifecycle Management Scoping Questions",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Blob Lifecycle Management Troubleshooter",
        "description": "Help us with a few inputs and give us couple of minutes to run automated diagnostics. We can help diagnose your problem without the need of opening a case.",
        "insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource. Please provide a sample blob path with this issue and ensure that it is in the approved format as suggested in the watermark."
    },
    "formElements": [
        {
            "id": "blob_path",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Sample blob path with tiering issues",
            "watermarkText": "'mycontainer/myblob.txt'",
            "required": false,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate local start time of the most recent occurrence",
            "required": true
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