<properties
         pageTitle="Scoping questions for Azure VM configuration protection failure"
         description="Scoping questions for Azure VM configuration protection failure"
         authors="ashishgangwar"
	     ms.author="asgang"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32574718"
         productPesIds="16370"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
	     articleId="4f18de2d-6ee6-4390-83ae-d79407886e99"
	ownershipId="Compute_SiteRecovery"
/>
# Questions Azure VM protection failure 
---
{
    "$schema": "SelfHelpContent",
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Azure VM configuration failure",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "vm_facing_issue",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "Which virtual machine is experiencing the problem?",
            "watermarkText": "Enter the name of the virtual machine(s)",
            "required": true
        },
        {
            "id": "jobID_Name",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Enter the failed Site Recovery job Activity ID:",
            "watermarkText": "Ex. cace7461-dd3c-4e38-b4db-38dc57fdee7b",
            "required": false
        },
        {
            "id": "Select_ErrorMessage",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Select the error message that you received:",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Connection cannot be established to Office 365 authentication",
                    "text": "Connection cannot be established to Office 365 authentication"
                },
                {
                    "value": "Installation failed with internal error",
                    "text": "Installation failed with internal error"
                },
                {
                    "value": "Snapshot operation failed due to no network connectivity on the virtual machine",
                    "text": " Snapshot operation failed due to no network connectivity on the virtual machine"
                },
                {
                    "value": "Installation of mobility agent failed due to unsupported OS",
                    "text": "Installation of mobility agent failed due to unsupported OS"
                },
                {
                    "value": "Azure VM is not in desired provisioning state",
                    "text": "Azure VM is not in desired provisioning state"
                },
                {
                    "value": "My error message is not listed here",
                    "text": "My error message is not listed here"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "Basic_troubleshooting_multiselect",
            "order": 4,
            "controlType": "multiselectdropdown",
            "displayLabel": "Select the troubleshooting steps you have completed:",
            "dropdownOptions": [
                {
                    "value": "VM Agent (WA Agent) has latest version",
                    "text": "VM Agent (WA Agent) has latest version"
                },
                {
                    "value": "VM OS version is supported",
                    "text": "VM OS version is supported"
                },
                {
                    "value": "VM has required  connectivity",
                    "text": "VM has required connectivity"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
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
