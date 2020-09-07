<properties
	pageTitle="Storage Blob recovery"
	description="Storage Blob recovery scoping question"
	authors="Passaree"
    ms.author="passap"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32608638,32612607"
	productPesIds="16459,16598"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	articleId="2ba85226-8c6e-4ecf-bcd1-f3f199c5c6f0"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>
# Recover deleted Blob
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Storage Blob recovery scoping question",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Is it possible to recover my accidently deleted blob?",
        "description": "Our blob recovery troubleshooter can help identify if it might be possible to recover your deleted blob.",
        "insightNotAvailableText": "Our troubleshooter could not find deletion history on the blob path your provided. Please ensure that it is in the format shown in the watermark."
    },
    "formElements": [
        {
            "id": "blob_path",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Blob path",
            "watermarkText": "'ContainerName/.../BlobName'",
            "required": true,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "justification",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Impact of deleted data for your business",
            "watermarkText": "Recovery of deleted data is a manual and time-consuming process. Please help us understand the business impact of the deleted data.",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate local time blob was deleted",
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
