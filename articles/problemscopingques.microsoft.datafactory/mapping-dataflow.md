<properties
    pageTitle="Azure mapping Data Flow issue info"
    description="Scoping questions to gather mapping data flow issues information"
    authors="hecepeda,vimals"
    ms.author="hecepeda"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32633533,32633532,32633535,32637157,32633536,32633537,32633539,32633540"
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
    "fileAttachmentHint": "Consider attaching the support files to help us triage your problem faster. From the Author and Deploy section, select the pipeline/dataflow having issues -> click ... (3 dots) -> Download Support Files",
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
            "displayLabel": "Provide the Pipeline or Activity RunIDs. (separate with commas)",
            "infoBalloonText": "Enter the RunId for the issue",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 1,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional context for the error message you are encountering",
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
