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
            "infoBalloonText": "Select alert type",
            "displayLabel": "What type of alerts have you configured?",
            "dropdownOptions": [
                {
                    "value": "Default Azure Monitor Alerts",
                    "text": "Default Azure Monitor Alerts"
                },
                {
                    "value": "Custom Log Alerts",
                    "text": "Custom Log Alerts"
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
            "id": "scenario_multiselect",
            "order": 2,
            "controlType": "multiselectdropdown",
            "infoBalloonText": "Select relevant scenario",
            "displayLabel": "For which scenario(s) is the issue being observed?:",
            "dropdownOptions": [
                {
                    "value": "Delete backup data",
                    "text": "Delete backup data"
                },
                {
                    "value": "Soft-delete disabled for vault",
                    "text": "Soft-delete disabled for vault"
                },
                {
                    "value": "Backup failure",
                    "text": "Backup failure"
                },
		{
                    "value": "Restore failure",
                    "text": "Restore failure"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
	{
            "id": "issue_type",
            "order": 3,
            "controlType": "dropdown",
            "infoBalloonText": "issue",
            "displayLabel": "Which is the issue that you are facing?",
            "dropdownOptions": [
                {
                    "value": "An alert was not fired as expected",
                    "text": "An alert was not fired as expected"
                },
                {
                    "value": "An alert was fired when it should not have",
                    "text": "An alert was fired when it should not have"
                },
		{
                    "value": "A notification was not received as expected",
                    "text": "A notification was not received as expected"
                },
                {
                    "value": "A notification was received when I should not have",
                    "text": "A notification was received when I should not have"
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
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true,
     "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "problem_description",
            "order": 5,
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
