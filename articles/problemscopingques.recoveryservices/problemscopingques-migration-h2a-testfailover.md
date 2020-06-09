<properties
         pageTitle="Scoping questions for Hyper-V VM  test failover failures"
         description="Scoping questions for Hyper-V VM test failover failures"
         authors="genlin"
         ms.author="asgang"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32680622"
         productPesIds="16370"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="b2fea7c7-05c3-471d-aa5a-b3daf4ac38d4"
	ownershipId="Compute_SiteRecovery"
/>
# Questions Hyper-V VM Test Failover Failures
---
{
    "$schema": "SelfHelpContent",
     "subscriptionRequired": true,
     "resourceRequired": true,
    "title": "Azure VM Test Failover failures",
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
            "watermarkText": "Enter the name of the affected virtual machines",
            "required": true
        },
        {
            "id": "jobID_Name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Enter the ID of failed Site Recovery job Activity:",
            "watermarkText": "Example. cace7461-dd3c-4e38-b4db-38dc57fdee7b",
            "required": false
        },
        {
            "id": "Select_ErrorMessage",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": " I am trying to run the test failover, but ",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "the test failover failed",
                    "text": " the test failover failed"
                },
                {
                    "value": "Test failover is stuck ",
                    "text": "the test failover is stuck "
                },
                {
                    "value": "Test failover succeeded but failed to get the desired IP",
                    "text": "the test failover succeeded but failed to get the desired IP"
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
