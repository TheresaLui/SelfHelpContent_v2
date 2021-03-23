<properties
	pageTitle="Azure Data Factory Pipeline Info"
	description="Scoping questions to gather Azure Data Factory pipeline information"
	authors="lisaliu,hecepeda"
	ms.author="lisaliu"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32629483,32637158,32637159,32680905,32629480,32629495,32637161,32740731, 32781334, 32680906, 32680904, 32637160, 32788106"
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
    "diagnosticCard": {
        "title": "Azure Pipeline Activity Troubleshooter",
        "description": "Our Pipeline Activity RunId Troubleshooter can help you troubleshoot and solve your problem.",
        "insightNotAvailableText": "Our troubleshooter did not detect the issues we were looking for in your resource. Refer to the help manual below to troubleshoot your problem."
    },
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "What time did the problem begin?",
            "required": true
        },
        {
            "id": "problem_run_id",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Is this a run time issue? If yes, Provide the Pipeline or Activity RunIds (separated by commas)",
			"diagnosticInputRequiredClients": "Portal",
            "required": true
        },
        {
            "id": "ir_type",
            "order": 3,
			"visibility": "null",
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
            "id": "problem_report_id",
            "order": 4,
			"visibility": "ir_type == Self-hosted IR",
            "controlType": "textbox",
            "displayLabel": "Please provide the ReportIDs from all nodes separated with commas. (see Solutions tab for guidance on how to obtain Report ID)",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 5,
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
