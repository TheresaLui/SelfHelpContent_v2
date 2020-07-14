<properties
         pageTitle="Scoping questions for Issue with Log Alerts"
         description="Scoping questions for Issue with  Log Alerts"
         authors="srinathvasireddy"
	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32632788"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
	 articleId="fb486471-0ba5-4453-b474-7287048b5396"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions for Issue with Log Analytics Alerts
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Issue with Log Analytics Alerts",
    "fileAttachmentHint": "",
     "diagnosticCard": {
        "title": "Issue with Log Analytics Alerts",
        "description": "These diagnostics will check for errors.",
        "insightNotAvailableText": "We didn't find any problems"
    },
    "formElements": [
        {
            "id": "basic_troubleshooting_multiselect",
            "order": 1,
            "controlType": "multiselectdropdown",
            "infoBalloonText": "Check <a href='https://aka.ms/Monitor-Backup-LA'>Log Analytics</a> article",
            "displayLabel": "Select the troubleshooting steps that you have performed:",
            "dropdownOptions": [
                {
                    "value": "Ensured Log Analytics is available in the specified region",
                    "text": "Ensured Log Analytics is available in the specified region"
                },
                {
                    "value": "Ensured Log Analytics is supported by your backup scenario",
                    "text": "Ensured Log Analytics is supported by your backup scenario"
                },
                {
                    "value": "Post configuration waited for 24hrs for initial data push to complete",
                    "text": "Post configuration waited for 24hrs for initial data push to complete"
                },
                {
                    "value": "Reviewed the limitations of Data Update frequency to LA",
                    "text": "Reviewed the limitations of Data Update frequency to LA"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
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
