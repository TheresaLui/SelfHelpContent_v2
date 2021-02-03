<properties
	pageTitle="Error relating to Azure Quantum Jobs"
	description="Scoping questions to capture more details about errors encountered while running jobs in Azure Quantum"
	ms.author="dasto"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32740182,32740183,32740185,32740187,32740190,32740191,32740193,32740194"
	productPesIds="17040"
	cloudEnvironments="public, fairfax, usnat, ussec"
	schemaVersion="1"
	articleId="problemscopingques-quantum-jobs"
	ownershipId="Azure_Quantum"
/>
# Error relating to Azure Quantum Jobs
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "Error relating to Azure Quantum Jobs",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "infoBalloonText": "Enter the approximate time you started to see the error.",
            "required": true
        },
        {
            "id": "problem_end_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem stop? (If ongoing, leave this field blank)",
            "infoBalloonText": "Enter when the error stopped, or leave blank if the issue is ongoing.",
            "required": false
        },
        {
            "id": "az_quantum_job_id",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Job Id(s) that this case relates to (if applicable)",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "Provide additional information about your issue. If available, please include the full error message and any stack traces you are receiving."
        }
    ]
}
---
