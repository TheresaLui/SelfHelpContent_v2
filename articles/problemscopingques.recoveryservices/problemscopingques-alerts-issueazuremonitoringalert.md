<properties
         pageTitle="Scoping questions for Issue with Azure Monitoring alerts (rule based)"
         description="Scoping questions for Issue with Azure Monitoring alerts (rule based)"
         authors="srinathvasireddy"
	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32632783"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
	articleId="581fcaaa-2d8f-4897-8dba-20e19a78926e"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions for Issue with Azure Monitoring alerts (rule based)
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Issue with Azure Monitoring alerts (rule based)",
    "fileAttachmentHint": "Please attach the screenshot of Alert screen filtered with timespan",
     "diagnosticCard": {
        "title": "Issue with Azure Monitoring alerts (rule based)",
        "description": "These diagnostics will check for errors.",
        "insightNotAvailableText": "We didn't find any problems"
    },
    "formElements": [
        {
            "id": "issue_type",
            "order": 1,
            "controlType": "dropdown",
            "infoBalloonText": "For more information see. Log alerts - <a href='https://aka.ms/AB-Alert-Tshooting'>'not received'</a>, <a href='https://aka.ms/AB-Alerts-fireunexpectedly'>'triggered unexpected'</a>, <a href='https://aka.ms/AB-Alerts-Delay'>'delays'</a>, <a href='https://aka.ms/AB-Alerts-Howto'>'How-to'</a>",
            "displayLabel": "Which type of issue you are facing?",
            "dropdownOptions": [
                {
                    "value": "Log alert not received (or was disabled)",
                    "text": "Log alert not received (or was disabled)"
                },
                {
                    "value": "Log alerts triggered unexpectedly",
                    "text": "Log alerts triggered unexpectedly"
                },
                {
                    "value": "Log alerts received with delays",
                    "text": "Log alerts received with delays"
                },
                {
                    "value": "How to Create, view, and manage log alerts",
                    "text": "How to Create, view, and manage log alerts"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true,
     "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true,
     "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": []
        }
    ],
    "$schema": "SelfHelpContent"
}
---
