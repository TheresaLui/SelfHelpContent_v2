<properties
         pageTitle="Scoping questions for System State backup performance"
         description="Scoping questions for System State backup performance"
         authors="srinathvasireddy"
	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32594867"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
	 articleId="03d5807f-181f-4e1b-a698-8f2744043e9b"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions System State backup performance
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "System State backup performance",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "System State backup performance",
        "description": "These diagnostics will check for errors.",
        "insightNotAvailableText": "We didn't find any problems"
    },
    "formElements": [
        {
            "id": "machine_name",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Which machine is experiencing the problem?",
            "watermarkText": "Enter the name of the Windows Server or Windows Client",
            "required": false
        },
        {
            "id": "performance_issue_type",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Are you experiencing performance issue with initial/incremental backup?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Initial (first) backup",
                    "text": "Initial (first) backup"
                },
                {
                    "value": "Incremental backup",
                    "text": "Incremental backup"
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
            "id": "backup_type",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Are you taking System State backup for an Azure VM?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
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
            "id": "job_time",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Since how long the job is running?",
            "watermarkText": "Ex. 18 hrs",
            "required": false
        },
        {
            "id": "basic_troubleshooting_multiselect",
            "order": 5,
            "controlType": "multiselectdropdown",
            "infoBalloonText": "Check slow backup <a href='https://aka.ms/AB-AA4dwtl'>Troubleshooting</a> article",
            "displayLabel": "Select the troubleshooting steps you have performed:",
            "dropdownOptions": [
                {
                    "value": "5-10% free volume space is available on scratch folder location",
                    "text": "5-10% free volume space is available on scratch folder location"
                },
                {
                    "value": "If antivirus is running, then exclusion rules are used",
                    "text": "If antivirus is running, then exclusion rules are used"
                },
                {
                    "value": "Network throttling is not configured on the machine",
                    "text": "Network throttling is not configured on the machine"
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
