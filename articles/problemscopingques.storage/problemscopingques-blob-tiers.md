<properties
	pageTitle="Blob tiers - Hot, Cool, Archive scoping questions"
	description="Blob tiers - Hot, Cool, Archive scoping questions"
	authors="passaree"
    ms.author="passap"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602719,32602732,32602720,32691059,32691060,32691061"
	productPesIds="16459,16598"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	articleId="4B46FE3E-420A-4916-B059-A6C939025930"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>
# Storage Access Tiers
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Blob tiers - Hot, Cool, Archive scoping question",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Why can I not set tiering on my blobs?",
        "description": "Our blob tier troubleshooter can help you troubleshoot and solve your problem.",
        "insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource. Please provide a sample blob path with this issue and ensure that it is in the approved format."
    },
    "formElements": [
        {
            "id": "blob_path",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Sample blob path with tiering issues",
            "watermarkText": "'ContainerName/.../BlobName'",
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