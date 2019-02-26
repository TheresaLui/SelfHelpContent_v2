<properties
	pageTitle="Unable to delete Blob or Container"
	description="Unable to delete Blob or Container scoping question"
	authors="Passaree"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602738"
	productPesIds="16459"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="947c84f0-2254-4392-ab29-1f5a2803b8a4"
/>
# Unable to delete Blob or Container
---
{
    "resourceRequired": true,
    "title": "Unable to delete Blob or Container scoping question",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "learn_more_text",
            "order": 1,
            "controlType": "infoblock",
            "content": "Please ensure that there is no lease or <a href='https://docs.microsoft.com/azure/virtual-machines/windows/storage-resource-deletion-errors'>VM attached to the blob or container</a> you are trying to delete."
        },
        {
            "id": "blob_or_container",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "Container name or Blob path",
            "watermarkText": "'ContainerName' or 'ContainerName/../BlobName' if specific to a container or blob",
            "required": false
        },
        {
            "id": "blob_container",
            "order": 3,
            "controlType": "multiselectdropdown",
            "displayLabel": "Blob Container",
            "watermarkText": "Choose an option",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionId}/resourceGroups/{resourceGroupName}/providers/Microsoft.Storage/storageAccounts/{accountName}/blobServices/default/containers?api-version=2018-07-01",
                "jTokenPath": "value",
                "textProperty": "id",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$"
            },
            "dropdownOptions": [
                {
                    "value": "NoBlobContainer",
                    "text": "Not specific to a blob container"
                }
            ],
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate time of the last deletion attempt",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide any additional details",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ]
}
---