<properties
	pageTitle="Storage blob recovery - soft delete"
	description="Storage blob recovery with soft delete scoping question"
	authors="Passaree"
    	ms.author="passap"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32608637, 32742781"
	productPesIds="16459, 16598"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	articleId="28C3054C-BDB6-41AC-9968-9EA4A458BC85"
	ownershipId="StorageMediaEdge_StorageBlobs"
/>
# Recover deleted blob with soft delete
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Storage Blob recovery scoping question",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Is it possible to recover my deleted blob with soft delete?",
        "description": "Our blob recovery troubleshooter can help identify if it might be possible to recover your deleted blob.",
        "insightNotAvailableText": "Our troubleshooter could not find deletion history on the blob path your provided. Please ensure that it is in the format shown in the watermark."
    },
    "formElements": [
        {
            "id": "blob_path",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Container/Blob path",
            "watermarkText": "'ContainerName/.../BlobName'",
            "required": false,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate local time container/blob was deleted",
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
