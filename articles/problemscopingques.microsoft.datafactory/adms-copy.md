<properties
	pageTitle="Azure Data Movement copy issue info"
	description="Scoping questions to gather Azure Data Movement copy issue information"
	authors="chez-charlie, hecepeda"
	ms.author="chez"
	selfHelpType="problemScopingQuestions"
    supportTopicIds="32629461, 32629463"
	productPesIds="15613"
	cloudEnvironments="public, Fairfax, usnat, ussec"
	schemaVersion="1"
    articleId="ff731302-5b98-42fd-98d3-73317cd531a0"
	ownershipId="AzureData_DataFactory"
/>

# Azure Data Movement Issue

---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Azure Data Movement copy issue info",
    "fileAttachmentHint": "Please attach JSON code for dataset, linked service and screen shots to help us triage your problem faster",
    "diagnosticCard": {
        "title": "Azure Copy Activity Troubleshooter",
        "description": "Our Copy Activity RunId Troubleshooter can help you troubleshoot and solve your problem.",
        "insightNotAvailableText": "Our troubleshooter did not detect the issues we were looking for in your resource. Refer to the help manual below to troubleshoot your problem."
    },
    "formElements": [
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Please briefly describe the issue",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [{"text": "Is it a new issue or regression? Is the issue intermittent or persistent?"}]
        },
        {
            "id": "error_message",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "What error message do you see?",
            "required": false
        },
        {
            "id": "source_name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "What's the source of the copy activity?",
            "required": false
        },
        {
            "id": "sink_name",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "What's the sink of the copy activity?",
            "required": false
        },
		{
            "id": "problem_run_id",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Is this a run time issue? If yes, Provide the Pipeline or Activity RunIds (separated by commas)",
            "diagnosticInputRequiredClients": "Portal",
            "required": true
        },
        {
            "id": "ir_type",
            "order": 6,
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
            "order": 7,
			"visibility": "ir_type == Self-hosted IR",
            "controlType": "textbox",
            "displayLabel": "Please provide the ReportIDs from all nodes separated with commas. (see Solutions tab for guidance on how to obtain the ReportID)",
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 8,
            "controlType": "datetimepicker",
            "displayLabel": "What time did the problem begin?",
            "required": true
        },
        {
            "id": "problem_end_time",
            "order": 9,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate time when the problem stopped occurring. If the issue is ongoing, leave this field blank",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
