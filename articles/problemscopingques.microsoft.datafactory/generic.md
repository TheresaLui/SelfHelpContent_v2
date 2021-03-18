<properties
	pageTitle="Azure Data Factory Generic Scoping Questions"
	description="Scoping questions to Distinguish V1 versus V2"
	authors="chez-charlie"
	ms.author="chez"
	selfHelpType="problemScopingQuestions"
    supportTopicIds="32629441, 32637149, 32629446, 32629439, 32629484, 32629521, 32742804"
	productPesIds="15613"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
    articleId="46507f35-8fd9-48ec-8d09-c3d93ce3ed02"
	ownershipId="AzureData_DataFactory"
/>

# Azure Data Factory Issue

---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Azure Data Factory Issue",
    "fileAttachmentHint": "Please attach JSON definition of your pipelines",
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
            "id": "df_version",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Which Version of Data Factory are you using?",
            "watermarkText": "Choose Data Factory Version",
            "dropdownOptions": [
                {
                    "value": "V2",
                    "text": "V2"
                },
                {
                    "value": "V1",
                    "text": "V1"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "factory_name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Name of the data factory",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "What time did the problem begin?",
            "required": true
        },
        {
            "id": "problem_end_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate time when the problem stopped occurring. If the issue is ongoing, leave this field blank",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
