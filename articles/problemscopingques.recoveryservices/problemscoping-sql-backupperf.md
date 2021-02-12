<properties
         pageTitle="Scoping questions for SQL database backup performance"
         description="Scoping questions for SQL database backup performance"
         authors="srinathvasireddy"
         ms.author="srinathvasireddy"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32605792"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="18b06d30-478c-4950-b3bc-5ed2dfecdd7d"
	ownershipId="StorageMediaEdge_Backup"
/>
# Scoping questions for SQL database backup performance
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "SQL database backup performance",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "SQL database backup performance",
        "description": "These diagnostics will check for errors.",
        "insightNotAvailableText": "We didn't find any problems"
    },
    "formElements": [
        {
            "id": "machine_name",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Which machine is experiencing the problem?",
            "watermarkText": "Select the virtual machine running SQL",
            "dynamicDropdownOptions": {
                     "uri": "/subscriptions/{subscriptionid}/resources?api-version=2018-05-01&$filter=resourceType eq 'Microsoft.Compute/virtualMachines' or resourceType eq 'Microsoft.ClassicCompute/virtualMachines'",
                     "jTokenPath": "value",
                     "textProperty": "name",
                     "valueProperty": "id",
                     "textPropertyRegex": ".*",
                     "defaultDropdownOptions": {
                           "value": "dont_know_answer",
                           "text": "Other or none of the above"
                     }
          },
           "required": false
        },
        {
            "id": "database_Name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Provide the name(s) of the databases whose backup is slow?",
            "watermarkText": "Enter database name(s) comma separated",
            "required": false
        },
        {
            "id": "backup_Type",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Which type of performance issue are you facing?",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "Slow backup during Full backup",
                    "text": "Slow backup during Full backup"
                },
                {
                    "value": "Slow backup during Log backup",
                    "text": "Slow backup during Log backup"
                },
                {
                    "value": "Slow backup during Differential backup",
                    "text": "Slow backup during Differential backup"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "jobID_Name",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Enter the long running job activity ID:",
            "watermarkText": "Ex. cace7461-dd3c-4e38-b4db-38dc57fdee7b",
            "required": false
        },
        {
            "id": "job_Running_Time",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Since how long the job is running?",
            "watermarkText": "Enter time in hours ex. 18hrs",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
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
