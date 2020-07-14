<properties
	pageTitle="Azure Data Movement general issue info"
	description="Scoping questions to gather Azure Data Movement general issue information"
	authors="sheldonfeng"
	ms.author="shelfeng"
	selfHelpType="problemScopingQuestions"
    supportTopicIds="32637153, 32629540, 32680904, 32680905, 32680906"
	productPesIds="15613"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
    articleId="add0db11-c89e-4110-8cee-bba530732c9d"
	ownershipId="AzureData_DataFactory"
/>

# Azure Data Movement Issue

---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Azure Data Movement general issue info",
    "fileAttachmentHint": "Please attach JSON code for dataset, linked service and screen shots to help us triage your problem faster",
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
            "id": "error_message",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "What error message do you see?",
            "required": false
        },
        {
            "id": "ir_type",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Which type of integration runtime are you using?",
            "watermarkText": "Choose an IR type",
            "dropdownOptions": [
                {
                    "value": "Azure IR",
                    "text": "Azure IR"
                },
                {
                    "value": "Self-hosted IR",
                    "text": "Self-hosted IR"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "sample_run_ids",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Is this a run time issue? If yes, please provide the RunIDs. (separate with commas)",
            "required": false
        },
        {
            "id": "df_version",
            "order": 5,
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
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "What time did the problem begin?",
            "required": true
        },
        {
            "id": "problem_end_time",
            "order": 7,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate time when the problem stopped occurring. If the issue is ongoing, leave this field blank",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
