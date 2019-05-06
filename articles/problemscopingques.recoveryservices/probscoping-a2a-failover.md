<properties
         pageTitle="Scoping questions for Azure VM failover failures"
         description="Scoping questions for Azure VM failover failure"
         authors="genlin"
         ms.author="asgang"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32574719"
         productPesIds="16370"
         cloudEnvironments="public"
         schemaVersion="1"
         articleId="2b342a85-2011-4b4d-b7d0-43639892e013"
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
            "displayLabel": "What is the OS version of the impacted Server?",
            "watermarkText": "Ex: Windows Server 2016, Ubuntu 16.04 LTS server kernel 4.10.0-14-generic to 4.10.0-32-generic",
            "required": true
        },
        {
            "id": "machine_name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Which machine is experiencing the problem?",
            "watermarkText": "Enter the name of the impacted machine",
            "required": true
        },
        {
            "id": "jobID_Name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Enter the failed Site Recovery job Activity ID:",
            "watermarkText": "Ex. cace7461-dd3c-4e38-b4db-38dc57fdee7b",
            "required": true
        },
        {
            "id": "Select_ErrorMessage",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": " I am trying to do failover, but ",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": " failover failed",
                    "text": " failover failed"
                },
                {
                    "value": "failover is stuck ",
                    "text": "failover is stuck "
                },
                {
                    "value": "failover succeeded but failback failed",
                    "text": " failover succeeded but failback failed"
                },
                {
                    "value": "ILB,NSG or Public IP were not replicated",
                    "text": "ILB, NSG or Public IP were not replicated"
                },
                 {
                    "value": "disks were missing post failover/failback",
                    "text": "disks were missing post failover/failback"
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
    ]
}
---
