<properties
         pageTitle="Scoping questions for Azure VM backup performance"
         description="Scoping questions for Azure VM backup performance"
         authors="srinathv"
	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32553281,32637321"
         productPesIds="15207,15571,15797,16454,16470,14749"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
	 articleId="7f7a167f-4e34-4592-bbe1-07b539f5fa8e"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions Azure VM backup performance
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Azure VM backup performance",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "vm_facing_issue",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Which virtual machine is experiencing problem?",
            "watermarkText": "Enter the name of the virtual machine",
	    "dynamicDropdownOptions": {
            "uri": "/subscriptions/{subscriptionid}/resources?api-version=2018-05-01&$filter=resourceType eq 'Microsoft.Compute/virtualMachines' or resourceType eq 'Microsoft.ClassicCompute/virtualMachines'",
       	    "jTokenPath": "value",
            "textProperty": "name",
            "valueProperty": "id",
            "textPropertyRegex": ".*",
	    "defaultDropdownOptions": {
                "value": "dont_know_answer",
                "text": "Other, don't know or not applicable"
            }
	    },
            "required": true
        },
        {
            "id": "Issue_Type",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Which type of performance issue you are facing",
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
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Enter the long running job activity ID:",
            "watermarkText": "Ex. cace7461-dd3c-4e38-b4db-38dc57fdee7b",
            "required": false
        },
        {
            "id": "Backup_Completeness",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Is the backup ever completed before?",
            "watermarkText": "Select",
            "dropdownoptions": [
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
            "id": "problem_description",
            "order": 6,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": []
        },
        {
            "id": "problem_start_time",
            "order": 7,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
