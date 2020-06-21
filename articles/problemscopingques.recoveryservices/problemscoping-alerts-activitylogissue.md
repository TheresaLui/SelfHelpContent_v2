<properties
         pageTitle="Scoping questions for issue with Activity Log alerts"
         description="Scoping questions for issue with Activity Log alerts"
         authors="srinathvasireddy"
		 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32632782"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
		 articleId="035e14d8-7eda-433a-8bb4-14d77e56def9"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions Issue with Activity Log alerts
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Issue with Activity Log alerts",
     "diagnosticCard": {
        "title": "Issue with Activity Log alerts",
        "description": "These diagnostics will check for errors.",
        "insightNotAvailableText": "We didn't find any problems"
    },
    "fileAttachmentHint": "Please attach the screenshot of Activity log alert screen filtered with timespan",
    "formElements": [
		{
            "id": "issue_type",
            "order": 1,
            "controlType": "dropdown",
            "infoBalloonText": "For more information see <a href='https://aka.ms/Configure-AlertsNotification-ActivityLogs'>Activity Log Alert</a>",
            "displayLabel": "Which type of issue you are facing?",
            "dropdownOptions": [
                {
                    "value": "Activity Log alert not received",
                    "text": "Activity Log alert not received"
                },
                {
                    "value": "Activity Log alerts triggered unexpectedly",
                    "text": "Activity Log alerts triggered unexpectedly"
                },
                {
                    "value": "Activity Log alerts received with delays",
                    "text": "Activity Log alerts received with delays"
                },
                {
                    "value": "How to Create, view, and manage Activity log alerts",
                    "text": "How to Create, view, and manage Activity log alerts"
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
            "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": []
        },
        {
            "id": "problem_start_time",
            "order": 3,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
