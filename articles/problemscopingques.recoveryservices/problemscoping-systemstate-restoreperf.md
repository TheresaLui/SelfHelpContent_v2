<properties
         pageTitle="Scoping questions for System State restore performance"
         description="Scoping questions for System State restore performance"
         authors="srinathvasireddy"
	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32632800"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
	 articleId="9182b0e1-cf2a-48a6-9b3d-9a4ae08bcf86"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions System State restore performance
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "System State restore performance",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "System State restore performance",
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
            "id": "restore_type",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Which type of recovery you are performing?",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "Recovering System State files to the same server",
                    "text": "Recovering System State files to the same server"
                },
                {
                    "value": "Recovering System State files to an alternate server",
                    "text": "Recovering System State files to an alternate server"
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
            "id": "problem_start_time",
            "order": 5,
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
