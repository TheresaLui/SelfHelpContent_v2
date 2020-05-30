<properties
	pageTitle="Azure Data Factory Pipeline Info"
	description="Scoping questions to gather Azure Data Factory pipeline information"
	authors="lisaliu,hecepeda"
	ms.author="lisaliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32629483,32637158,32637159,32629480,32629495,32637161,32740731"
	productPesIds="15613"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="BE3D6801-3F87-41BC-ACF9-B9DA8A86C55C"
	ownershipId="AzureData_DataFactory"
/>

# Azure Data Factory Pipeline Info

---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Azure Data Factory Pipeline Info",
    "fileAttachmentHint": "Please attach JSON code for dataset, linked service, and output of activity run to help us triage your problem faster",
    "formElements": [
        {
            "id": "df_version",
            "order": 1,
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
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "What time did the problem begin?",
            "required": true
        },
        {
            "id": "problem_end_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate time when the problem stopped occurring. If the issue is ongoing, leave this field blank",
            "required": false
        },
        {
            "id": "pipeline_name",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Name of the problem pipeline(s) (separate with commas)",
            "required": false
        },
        {
            "id": "pipeline_json_code",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "JSON code of the affected pipeline",
            "required": false
        },
        {
            "id": "sample_pipeline_run_ids",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "Sample problem pipeline RunIDs (separate with commas)",
            "required": false
        },
        {
            "id": "sample_activity_run_ids",
            "order": 7,
            "controlType": "textbox",
            "displayLabel": "Sample problem activity RunIDs (separate with commas)",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 8,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional details about the issue",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Exact error message if applicable"
                },
                {
                    "text": "Is the issue intermittent or persistent?"
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
