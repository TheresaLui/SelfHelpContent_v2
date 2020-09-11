<properties
	pageTitle="Error relating to Azure Quantum Jobs"
	description="Scoping questions to capture more details about errors encountered while running jobs in Azure Quantum"
	ms.author="dasto"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32740178,3270182,32740183,32740185,32740187,32740190,32740191,32740193,32740194"
	productPesIds="17040"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="problemscopingques-quantum-jobs"
	ownershipId="AzureCompute_AzureQuantum"
/>
# Error relating to Azure Quantum Jobs
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Error relating to Azure Quantum Jobs",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "infoBalloonText": "Enter the approximate time you started to see the error.",
            "required": true,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "problem_end_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem stop? (If ongoing, leave this field blank)",
            "infoBalloonText": "Enter when the error stopped, or leave blank if the issue is ongoing.",
            "required": false,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "az_quantum_job_id",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "If applicable, please share the Job Id(s) that this case relates to.",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional context for the error message you are encountering.",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "Always provide the full error text from the underlying client library (e.g., SqlClient), not the general error from your client application.  If available, include the client stack trace as well."
        }
    ]
}
---
