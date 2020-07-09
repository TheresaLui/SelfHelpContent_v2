<properties
         pageTitle="Scoping questions for Azure VM Restore performance"
         description="Scoping questions for Azure VM Restore performance"
         authors="srinathvasireddy"
	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32612998,32637327"
         productPesIds="15207,14749,15571,15797,16454,16470"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
	 articleId="9a98fd5d-c64c-4d29-9f4d-fd53e64b5c0b"
	 ownershipId="StorageMediaEdge_Backup"
/>
# Questions Azure VM Restore performance
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Azure VM Restore performance",
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
                    "value": "Slow restore during create new virtual machine operation",
                    "text": "Slow restore during create new virtual machine operation"
                },
                {
                    "value": "Slow restore during restore disk operation",
                    "text": "Slow restore during restore disk operation"
                },
                {
                    "value": "Slow restore during restore existing disks operation",
                    "text": "Slow restore during restore existing disks operation"
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
            "id": "job_Running_Time",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Since how long the job is running?",
            "watermarkText": "Enter time in hours ex. 18hrs",
            "required": false
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
        },
        {
            "id": "problem_start_time",
            "order": 6,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
