<properties
         pageTitle="Scoping questions for Azure VM failover failures"
         description="Scoping questions for Azure VM failover failure"
         authors="genlin"
         ms.author="asgang"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32574719"
         productPesIds="16370"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="2b342a85-2011-4b4d-b7d0-43639892e013"
	ownershipId="Compute_SiteRecovery"
/>
# Questions Azure VM Fail-over Failures 
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Azure VM Failover failures",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "os_version",
            "order": 1,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "What is the OS version of the affected virtual machine?",
            "watermarkText": "Example: Windows Server 2016, Ubuntu 16.04 LTS server kernel 4.10.0-14-generic to 4.10.0-32-generic",
            "required": false
        },
        {
            "id": "machine_name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Which virtual machines are experiencing the problem?",
            "watermarkText": "Enter the name of the impacted virtual machine",
            "required": true
        },
        {
            "id": "jobID_Name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Enter the ID of failed Site Recovery job activity:",
            "watermarkText": "Example. cace7461-dd3c-4e38-b4db-38dc57fdee7b",
            "required": false
        },
        {
            "id": "Select_ErrorMessage",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": " I am trying to do the failover, but ",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "the failover failed",
                    "text": " the failover failed"
                },
                {
                    "value": "failover is stuck ",
                    "text": "the failover is stuck "
                },
                {
                    "value": "failover succeeded but failback failed",
                    "text": " the failover succeeded but the failback failed"
                },
                {
                    "value": "ILB,NSG or Public IP were not replicated",
                    "text": "Internal load balancing, Network Security Groups or Public IP were not replicated"
                },
                {
                    "value": "disks were missing post failover/failback",
                    "text": "disks were missing post failover or failback"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 5,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
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
