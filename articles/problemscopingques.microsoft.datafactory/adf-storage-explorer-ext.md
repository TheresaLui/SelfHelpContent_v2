<properties
	pageTitle="ADF Storage Explorer Extension"
	description="Scoping questions to gather ADF Sotrage Explorer and ADF related data"
	authors="hecepeda"
	ms.author="hecepeda"
	selfHelpType="problemScopingQuestions"
    supportTopicIds="32783473"
	productPesIds="15613"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
    articleId="ADFStorageExplorerExt.md"
	ownershipId="AzureData_DataFactory"
/>

# Azure Data Factory Extension for Storage Explorer

---
{
    "resourceRequired": false,
    "subscriptionRequired": true,
    "title": "ADF Storage Explorer Extension",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Please briefly describe the issue",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Is it a new issue or regression?"
                },
                {
                    "text": "Is the issue intermittent or persistent?"
                }
            ]
        },
        {
            "id": "storage_explorer_version",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "What is your version of Storage Explorer?",
            "required": true
        },
        {
            "id": "ADF_extension_version",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "What is your version of ADF extension? ?",
            "required": false
        },
        {
            "id": "OS_Type",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Which type of operating system are you using?",
            "watermarkText": "Choose an OS type",
            "dropdownOptions": [
                {
                    "value": "Windows",
                    "text": "Windows"
                },
                {
                    "value": "Linux",
                    "text": "Linux"
                },
                {
                    "value": "Mac",
                    "text": "Mac"
                }
            ],
            "required": true
        },
		{
            "id": "storage_explorer_id",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Please provide your Storage Explorer support ID (Located on About window using Help menu)",
            "required": true
        },
        {
            "id": "error_message",
            "order": 6,
            "controlType": "multilinetextbox",
            "displayLabel": "What error message do you see?",
            "required": false
        },
        {
            "id": "Data_Source",
            "order": 7,
            "controlType": "dropdown",
            "displayLabel": "What is the source of the copy activity?",
            "watermarkText": "Supported Sources",
            "dropdownOptions": [
                {
                    "value": "S3",
                    "text": "Amazon S3"
                },
                {
                    "value": "ADLSGen2",
                    "text": "ADLS Gen 2"
                },
                {
                    "value": "Azure Blob",
                    "text": "Blob"
                }
            ],
            "required": true
        },
        {
            "id": "Data_Sink",
            "order": 7,
            "controlType": "dropdown",
            "displayLabel": "What is the sink (destination) of the copy activity?",
            "watermarkText": "Supported Sinks",
            "dropdownOptions": [
                {
                    "value": "ADLSGen2",
                    "text": "ADLS Gen 2"
                },
                {
                    "value": "Azure Blob",
                    "text": "Blob"
                }
            ],
            "required": true
        },
        {
            "id": "problem_run_id",
            "order": 8,
            "controlType": "textbox",
            "displayLabel": "Provide the Copy Activity RunId if you have one.",
            "infoBalloonText": "Enter the RunId for the issue.",
            "required": false,
        },
        {
            "id": "problem_start_time",
            "order": 9,
            "controlType": "datetimepicker",
            "displayLabel": "What time did the problem begin?",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
