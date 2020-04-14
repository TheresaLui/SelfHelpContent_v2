<properties
         pageTitle="Scoping questions for Azure File Share restore performance issue"
         description="Scoping questions for Azure File Share restore performance issue"
         authors="srinathvasireddy"
	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32612215"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
	 articleId="715505fa2-821e-4988-8b3d-d160e70e6ac9"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions for Azure File Share restore performance issue
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Azure File Share restore performance issue",
    "fileAttachmentHint": "",
     "diagnosticCard": {
        "title": "Azure File Share restore performance issue",
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
            "required": false
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
            "id": "restore_Type",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Select the Recovery Destination type:",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "Original Location",
                    "text": "Original Location"
                },
                {
                    "value": "Alternate Location",
                    "text": "Alternate Location"
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
            "id": "JobID_Name",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Enter the long running job activity ID:",
            "watermarkText": "Ex. cace7461-dd3c-4e38-b4db-38dc57fdee7b",
            "required": false
        },
        {
            "id": "Data_types",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Restoring a File Share that contains:",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "Large number of directories with few number of files",
                    "text": "Large number of directories with few number of files"
                },
                {
                    "value": "Large number of directories with large number of files",
                    "text": "Large number of directories with large number of files"
                },
                {
                    "value": "Small number of directories with few number of files",
                    "text": "Small number of directories with few number of files"
                },
                {
                    "value": "Small number of directories with large number of files ",
                    "text": "Small number of directories with large number of files "
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "Data_hierarchy",
            "order": 6,
            "controlType": "dropdown",
            "infoBalloonText": "Note: Restoring File Share with fewer directories is faster than File Share with large number of directories",
            "displayLabel": "Describe the directory to file ratio:",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "Large number of directories with few number of files",
                    "text": "Large number of directories with few number of files"
                },
                {
                    "value": "Large number of directories with large number of files",
                    "text": "Large number of directories with large number of files"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "Share_use_status",
            "order": 7,
            "controlType": "dropdown",
            "infoBalloonText": "Note: If other applications are consuming File Share IOPS then it could impact File Share restore performance",
            "displayLabel": "Are other applications using the same File share?",
            "watermarkText": "Select",
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
            "required": false
        },
        {
            "id": "job_Running_Time",
            "order": 8,
            "controlType": "textbox",
            "displayLabel": "Since how long the job is running?",
            "watermarkText": "Enter time in hours ex. 18hrs",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 9,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": []
        },
        {
            "id": "problem_start_time",
            "order": 10,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true,
     "diagnosticInputRequiredClients": "Portal"
        }
    ],
    "$schema": "SelfHelpContent"
}
---
