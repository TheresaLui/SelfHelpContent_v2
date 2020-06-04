<properties
         pageTitle="Scoping questions for Issue with Backup Alerts (email)"
         description="Scoping questions for Issue with Backup Alerts (email)"
         authors="srinathvasireddy"
	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32632784"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
	 articleId="52ac74b2-053d-4905-b2d4-f1940fb208c2"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions for Issue with Backup Alerts (email)
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Issue with Backup Alerts (email)",
    "fileAttachmentHint": "Please attach the screenshot of Backup Alerts screen filtered with timespan",
     "diagnosticCard": {
        "title": "Issue with Backup Alerts (email)",
        "description": "These diagnostics will check for errors.",
        "insightNotAvailableText": "We didn't find any problems"
    },
    "formElements": [
        {
            "id": "issue_type",
            "visibility": "null",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Which type of issue you are facing?",
            "dropdownOptions": [
                {
                    "value": "Unable to see backup alerts in Azure portal",
                    "text": "Unable to see backup alerts in Azure portal"
                },
                {
                    "value": "Not receiving notification for backup alerts",
                    "text": "Not receiving notification for backup alerts"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "alert_scenario",
            "visibility": "issue_type == Unable to see backup alerts in Azure portal",
            "order": 2,
            "controlType": "multiselectdropdown",
            "infoBalloonText": "Check backup <a href='https://aka.ms/BKP-RSVAlert-Scenarios'>Alert scenarios </a> article",
            "displayLabel": "For which alertable scenarios you are not seeing alerts?",
            "dropdownOptions": [
                {
                    "value": "Backup/Restore failures",
                    "text": "Backup/Restore failures"
                },
                {
                    "value": "Backup succeeded with warnings for Azure Backup Agent (MAB)",
                    "text": "Backup succeeded with warnings for Azure Backup Agent (MAB)"
                },
                {
                    "value": "Stop protection with retain data",
                    "text": "Stop protection with retain data"
                },
                {
                    "value": "Stop protection with delete data",
                    "text": "Stop protection with delete data"
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
            "id": "backup_solutions",
            "visibility": "issue_type == Unable to see backup alerts in Azure portal",
            "order": 3,
            "controlType": "multiselectdropdown",
            "infoBalloonText": "Note: Alerts from System Center Data Protection Manager (SC-DPM) and Microsoft Azure Backup Server (MABS) are NOT display in backup alerts",
            "displayLabel": "For which Azure Backup solution you are not seeing alerts?",
            "dropdownOptions": [
                {
                    "value": "Azure VM backups",
                    "text": "Azure VM backups"
                },
                {
                    "value": "Azure File backups",
                    "text": "Azure File backups"
                },
                {
                    "value": "Azure workload backups such as SQL",
                    "text": "Azure workload backups such as SQL"
                },
                {
                    "value": "Azure Backup agent (MAB)",
                    "text": "Azure Backup agent (MAB)"
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
            "id": "alert_type",
            "visibility": "issue_type == Unable to see backup alerts in Azure portal",
            "order": 4,
            "controlType": "multiselectdropdown",
            "displayLabel": "Which type of alerts you are not seeing?",
            "dropdownOptions": [
                {
                    "value": "Critical",
                    "text": "Critical"
                },
                {
                    "value": "Warning",
                    "text": "Warning"
                },
                {
                    "value": "Informational",
                    "text": "Informational"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
        },
        {
            "id": "basic_troubleshooting_multiselect",
            "visibility": "issue_type == Not receiving notification for backup alerts",
            "order": 5,
            "controlType": "multiselectdropdown",
            "infoBalloonText": "Check <a href='https://aka.ms/Monitor-JobsAlert-RSV'>Backup Alerts</a> article",
            "displayLabel": "Select the troubleshooting steps that you have performed:",
            "dropdownOptions": [
                {
                    "value": "Ensured the email address is correct in the Configure notification tab",
                    "text": "Ensured the email address is correct in the Configure notification tab"
                },
                {
                    "value": "I receive alerts for Per Alert, but not for Hourly digest",
                    "text": "I receive alerts for Per Alert, but not for Hourly digest"
                },
                {
                    "value": "I receive alerts for Hourly digest, but not for Per Alert",
                    "text": "I receive alerts for Hourly digest, but not for Per Alert"
                },
                {
                    "value": "I do not receive alerts either for Per Alert or Hourly digest",
                    "text": "I do not receive alerts either for Per Alert or Hourly digest"
                },
                {
                    "value": "I changed email address, but still do not receive alerts",
                    "text": "I changed email address, but still do not receive alerts"
                },
                {
                    "value": "I changed email address, started receiving alerts",
                    "text": "I changed email address, started receiving alerts"
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
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true,
     "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "problem_description",
            "order": 7,
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
