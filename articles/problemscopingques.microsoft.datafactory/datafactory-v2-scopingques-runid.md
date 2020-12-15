<properties
    pageTitle="I am having Pipeline/Trigger Run Issue"
    description="Scoping questions to capture more details about Pipeline and Trigger run issues."
    authors="samiranshah"
    ms.author="samirans"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32629472,32629491,32680901,32637152,32749442,32749443,32749444,32749445,32749446,32749447"
    productPesIds="15613"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="DataFactoryRunIdScopingQues"
	ownershipId="AzureData_DataFactory"
/>

# Data Factory Pipeline and Trigger Run
---
{
    "$schema": "SelfHelpContent",
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "I am having Pipeline/Trigger Run Issue",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Azure Data Factory RunId Troubleshooter",
        "description": "Our Azure Data Factory RunId Troubleshooter can help you troubleshoot and solve your problem.",
        "insightNotAvailableText": "Our troubleshooter did not detect the issues we were looking for in your resource. Refer to the help manual below to troubleshoot your problem."
    },
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
            "id": "problem_run_id",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Provide the Pipeline or Activity RunId.",
            "infoBalloonText": "Enter the RunId for the issue.",
            "required": true,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide additional context for the error message you are encountering.",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ]
}
---
