<properties
         pageTitle="Scoping questions for Azure VM Restore failure for Linux"
         description="Scoping questions for Azure VM Restore failure for Linux"
         authors="srinathvasireddy"
	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32553297"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
	articleId="32149b9d-e51c-45cd-8efb-642687f5b75d"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions Azure VM Restore failure for Linux 
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Azure VM Restore failure for Linux",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "vm_facing_issue",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Which virtual machine is experiencing the problem?",
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
            "id": "JobID_Name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Enter the failed restore job activity ID:",
            "watermarkText": "Ex. cace7461-dd3c-4e38-b4db-38dc57fdee7b",
            "required": false
        },
        {
            "id": "Restoration_Type",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Which type of restore are you performing?",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "Restoring VMs in Azure Portal",
                    "text": "Restoring VMs in Azure Portal"
                },
                {
                    "value": "Recovering files from Azure VMs backups",
                    "text": "Recovering files from Azure VMs backups"
                },
                {
                    "value": "Restore encrypted VMs",
                    "text": "Restore encrypted VMs"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": []
        },
        {
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "Problem start time",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
