<properties
	pageTitle="Storage File connectivity or performance issue"
	description="Storage File connectivity or performance scoping question"
	authors="Passaree"
    ms.author="passap"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32602759,32602770,32602761,32602762"
	productPesIds="16460"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="f55638b4-3688-4399-a0f6-dd6ef04717c9"
/>
# Storage File connectivity or performance issue
---
{
    "resourceRequired": true,
    "title": "Storage File connectivity or performance scoping question",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate start time of the most recent occurrence",
            "required": true,
            "diagnosticInputRequiredClients": "Portal,ASC"
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
            "required": false,
            "useAsAdditionalDetails": true
        }
    ],
    "diagnosticCard": "What caused my Azure Files connectivity issue?"
}
---
