<properties
	pageTitle="Storage Blob recovery"
	description="Storage Blob recovery scoping question"
	authors="Passaree"
    ms.author="passap"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32608638"
	productPesIds="16459"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="2ba85226-8c6e-4ecf-bcd1-f3f199c5c6f0"
/>
# Recover deleted Blob
---
{
    "resourceRequired": false,
    "title": "Storage Blob recovery scoping question",
    "fileAttachmentHint": "",
    "diagnosticCard": {
		"title": "Is it possible to recover my accidently deleted blob?",
    	"description": "Our blob recovery troubleshooter can help you troubleshoot and solve your problem.",
    	"insightNotAvailableText": "Our troubleshooter could not find your deleted blob. You can enable [soft delete for Azure Storage blobs](https://docs.microsoft.com/azure/storage/blobs/storage-blob-soft-delete) to ensure that accidentally deleted blobs will be recoverable in the future. ."
	},
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate local time Blob was deleted",
            "required": true,
            "diagnosticInputRequiredClients": "Portal,ASC"
        },
        {
            "id": "blob_path",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Blob path",
            "watermarkText": "'ContainerName/.../BlobName'",
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
    ]
}
---
