<properties
         pageTitle="Scoping questions for Azure backup server backup perf"
         description="Scoping questions for Azure backup server backup perf"
         authors="srinathvasireddy"
	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32553282,32553278"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
  	 articleId="c7e81485-c8d4-44d9-8abd-adea1ca94875"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions Azure backup server backup performance
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Azure backup server backup is taking longer",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Azure backup server backup is taking longer",
        "description": "These diagnostics will check for errors.",
        "insightNotAvailableText": "We didn't find any problems"
    },
    "formElements": [
        {
            "id": "issue_Type",
            "visibility": "null",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Select the backup type:",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "Backup to cloud is slow",
                    "text": "Backup to cloud is slow"
                },
                {
                    "value": "Backup to disk is slow",
                    "text": "Backup to disk is slow"
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
            "id": "mab_version",
            "order": 2,
            "visibility": "null",
            "controlType": "textbox",
            "infoBalloonText": "You can find version information from Microsoft Azure Backup Server Console\\Help\\About",
            "displayLabel": "What is the software version of Microsoft Azure Backup Server?",
            "watermarkText": "ex. version 12.0.332.0.",
            "required": false
        },
        {
            "id": "error_message",
            "order": 3,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "Provide the error message that you are seeing:",
            "watermarkText": "Copy and paste error message that you see in console",
            "required": false
        },
        {
            "id": "Basic_troubleshooting_multiselect",
            "order": 4,
            "visibility": "issue_Type == Backup to cloud is slow",
            "controlType": "multiselectdropdown",
            "infoBalloonText": "Check Azure Backup server backup <a href='https://aka.ms/AB-MABS-troubleshoot'>Troubleshooting</a> article",
            "displayLabel": "Select the troubleshooting steps that you have performed:",
            "dropdownOptions": [
                {
                    "value": "Azure Backup agent is latest",
                    "text": "Azure Backup agent is latest"
                },
                {
                    "value": "Ensured there is sufficient disk space to restore the data",
                    "text": "Ensured there is sufficient disk space to restore the data"
                },
                {
                    "value": "If antivirus is running, then exclusion rules are used",
                    "text": "If antivirus is running, then exclusion rules are used"
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
            "order": 5,
            "visibility": "null",
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true,
     "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "problem_description",
            "order": 6,
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
