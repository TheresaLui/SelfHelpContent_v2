<properties
         pageTitle="Scoping questions for VMM server addition failure"
         description="Scoping questions for VMM server addition failure"
         authors="ashishgangwar, TobyTu"
	     ms.author="asgang"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32634432"
         productPesIds="16370"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
	     articleId="881fcef2-0569-437b-bcda-0eede66b5dd1"
	ownershipId="Compute_SiteRecovery"
/>

# Add or Register a VMM Server
---
{
    "$schema": "SelfHelpContent",
     "subscriptionRequired": true,
     "resourceRequired": true,
    "title": "Add or Register a VMM Server",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "vmm_name",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Provide name of the VMM server that you are having issues with",
            "watermarkText": "Enter name(s) to scope down quickly",
            "required": true
        },
        {
            "id": "error_id",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Provide error ID or job ID of the add or register operation",
            "watermarkText": "Enter in the error ID or job ID",
            "required": false
        },
        {
            "id": "trouble_action",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "I am trying to install the provider on the VMM, but",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "The provider is not executing",
                    "text": "The provider is not executing"
                },
                {
                    "value": "The installation fails",
                    "text": "The installation fails"
                },
                {
                    "value": "The VMM is not showing on the portal",
                    "text": "The VMM is not showing on the portal"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "tried_steps",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "I have gone through steps provided in the following articles",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Prepare on-premises Hyper-V servers",
                    "text": "Prepare on-premises Hyper-V servers"
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
            "watermarkText": "Enter in local time",
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
