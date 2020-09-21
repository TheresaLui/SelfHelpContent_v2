<properties
	pageTitle="Error relating to Azure Quantum Providers"
	description="Scoping questions to capture more details about errors encountered with provider-related issues in Azure Quantum"
	ms.author="dasto"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32740195,32740192,32740186"
	productPesIds="17040"
	cloudEnvironments="public"
	schemaVersion="1"
	articleId="problemscopingques-quantum-providers"
	ownershipId="AzureCompute_AzureQuantum"
/>
# Error relating to Azure Quantum Providers
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Error relating to Azure Quantum Provider",
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
            "id": "az_quantum_provider",
            "order": 3,
            "controlType": "multiselectdropdown",
            "displayLabel": "If your case relates to one or more specific provider(s), please share the provider name(s) with us.",
            "dropdownOptions": [{
                    "value": "1Qloud",
                    "text": "1Qloud Optimization Platform"
                }, {
                    "value": "Honeywell",
                    "text": "Honeywell Quantum Solutions"
                }, {
                    "value": "IonQ",
                    "text": "IonQ"
                }, {
                    "value": "MS Quantum",
                    "text": "Microsoft Quantum Solutions"
                }, {
                    "value": "Quantum Circuits",
                    "text": "Quantum Circuits, Inc."
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional context for the error message you are encountering.",
            "required": true,
            "useAsAdditionalDetails": true,
            "watermarkText": "Always provide the full error text from the underlying client library, not the general error from your client application.  If available, include the client stack trace as well."
        }
    ]
}
---
