<properties
         pageTitle="Scoping questions for Azure File Share backup performance issue"
         description="Scoping questions for Azure File Share backup performance issue"
         authors="srinathvasireddy"
	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32612211"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
	 articleId="78d9d4fe-4e02-4f16-9e66-ab9529f5c0ae"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions for Azure File Share backup performance issue
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Azure File Share backup performance issue",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Azure File Share backup performance diagnostics",
        "description": "These diagnostics will check for errors.",
        "insightNotAvailableText": "We didn't find any problems"
    },
    "formElements": [
        {
            "id": "storage_account_name",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Which storage account(s) is experiencing the problem?",
            "watermarkText": "Enter the name of the storage account(s)",
	          "dynamicDropdownOptions": {
            "uri": "/subscriptions/{subscriptionid}/resources?api-version=2018-05-01&$filter=resourceType eq 'Microsoft.Storage/storageAccounts' or resourceType eq 'Microsoft.ClassicStorage/storageAccounts'",
            "jTokenPath": "value",
            "textProperty": "name",
            "valueProperty": "id",
            "textPropertyRegex": ".*",
	    "defaultDropdownOptions": {
                "value": "dont_know_answer",
                "text": "Other, don't know or not applicable"
            }
          },
            "required": false,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "fileshare_Name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Provide the name(s) of the File Share for which you are facing performance issue:",
            "watermarkText": "Enter file share name(s) comma separated",
            "required": false
        },
        {
            "id": "Issue_Type",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Which type of performance issue you are facing?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Slow backup during initial (first) backup",
                    "text": "Slow backup during initial (first) backup"
                },
                {
                    "value": "Slow backup during incremental backup",
                    "text": "Slow backup during incremental backup"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "JobID_Name",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Enter the long running job activity ID:",
            "watermarkText": "Ex. cace7461-dd3c-4e38-b4db-38dc57fdee7b",
            "required": false
        },
        {
            "id": "Backup_Completeness",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Is the backup ever completed before?",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "Value": "Yes",
                    "Text": "Yes"
                },
                {
                    "Value": "No",
                    "Text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "job_Running_Time",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "Since how long the job is running?",
            "watermarkText": "Enter time in hours ex. 18hrs",
            "required": false
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
        },
        {
            "id": "problem_start_time",
            "order": 8,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
