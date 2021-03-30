<properties
    pageTitle="Azure mapping Data Flow issue info"
    description="Scoping questions to gather mapping data flow issues information"
    authors="hecepeda,vimals"
    ms.author="hecepeda"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32633533,32633532,32633535,32637157,32633536,32633537,32633539,32633540,32786125"
    productPesIds="15613"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="mapping-dataflow"
    ownershipId="AzureData_DataFactory"
/>
# Azure mapping Data Flow issue info
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Azure mapping Data Flow issue info",
    "fileAttachmentHint": "Consider attaching the support files to help us triage your problem faster. From the Author and Deploy section, select the pipeline/dataflow having issues, then click ... (3 dots) and choose Download Support Files",
    "diagnosticCard": {
        "title": "Azure mapping Data Flow Troubleshooter",
        "description": "Our Azure mapping Data Flow RunId Troubleshooter can help you troubleshoot and solve your problem.",
        "insightNotAvailableText": "Our troubleshooter did not detect the issues we were looking for in your resource. Refer to the help manual below to troubleshoot your problem."
    },
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "infoBalloonText": "Enter the approximate time you started to see the error",
            "required": true
        },
        {
            "id": "problem_run_id",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Provide the Data flow activity RunID",
            "infoBalloonText": "Enter the RunId for the issue",
			"diagnosticInputRequiredClients": "Portal",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Provide additional context for the error message you are encountering",
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
        }
    ]
}
---
