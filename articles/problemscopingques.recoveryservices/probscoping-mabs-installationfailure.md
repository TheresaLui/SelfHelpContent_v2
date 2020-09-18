<properties
         pageTitle="Scoping questions for Azure backup server Installation or Configuration Failures"
         description="Scoping questions for Azure backup server Installation or Configuration Failures"
         authors="srinathvasireddy"
	 ms.author="srinathv"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32570754"
         productPesIds="15207"
         cloudEnvironments="public, fairfax, usnat, ussec"
         schemaVersion="1"
	 articleId="26a0819f-c924-4d9a-9735-818aac4dc67e"
	ownershipId="StorageMediaEdge_Backup"
/>
# Questions Azure backup server Installation or Configuration Failures
---
{
    "resourceRequired": true,
    "subscriptionRequired": true,
    "title": "Azure backup server Installation or Configuration Failures",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "installation_Type",
            "visibility": "null",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Is this a new/upgrade installation?",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "New",
                    "text": "New"
                },
                {
                    "value": "Upgrade from V1 to V2",
                    "text": "Upgrade from V1 to V2"
                },
                {
                    "value": "Upgrade from V2 to V3",
                    "text": "Upgrade from V2 to V3"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "issue_Type",
            "visibility": "installation_Type == New",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "At what point is the installation failing?",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "Microsoft Azure Recovery Service agents failed to install",
                    "text": "Microsoft Azure Recovery Service agents failed to install"
                },
                {
                    "value": "SQL components failed to install",
                    "text": "SQL components failed to install"
                },
                {
                    "value": "Microsoft Azure backup(DPM) software failed to install",
                    "text": "Microsoft Azure backup(DPM) software failed to install"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "os_version",
            "order": 3,
            "visibility": "issue_Type == Microsoft Azure Recovery Service agents failed to install || issue_Type == SQL components failed to install || issue_Type == Microsoft Azure backup(DPM) software failed to install",
            "controlType": "textbox",
            "displayLabel": "What is the OS version of the dedicated server?",
            "watermarkText": "ex. Windows 2012 R2",
            "required": false
        },
        {
            "id": "registration_Type",
            "order": 4,
            "visibility": "issue_Type == Microsoft Azure Recovery Service agents failed to install",
            "controlType": "dropdown",
            "displayLabel": "Is this an initial-registration/re-registration issue?",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "Initial-registration",
                    "text": "Initial-registration"
                },
                {
                    "value": "Re-registration",
                    "text": "Re-registration"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": false
        },
        {
            "id": "basic_troubleshooting_multiselect",
            "order": 5,
            "visibility": "issue_Type == Microsoft Azure Recovery Service agents failed to install",
            "controlType": "multiselectdropdown",
            "displayLabel": "Select the troubleshooting steps you have performed:",
            "dropdownOptions": [
                {
                    "value": "OS version is supported for backup",
                    "text": "OS version is supported for backup"
                },
                {
                    "value": "If firewall is used, then required URLs are whitelisted",
                    "text": "If firewall is used, then required URLs are whitelisted"
                },
                {
                    "value": "Machine has Internet connectivity",
                    "text": "Machine has Internet connectivity"
                },
                {
                    "value": "If antivirus is running, then exclusion rules are used",
                    "text": "If antivirus is running, then exclusion rules are used"
                },
                {
                    "value": ".NET framework version is at least 4.6.2",
                    "text": ".NET framework version is at least 4.6.2"
                },
                {
                    "value": "Server is not registered with another vault",
                    "text": "Server is not registered with another vault"
                },
                {
                    "value": "Ensure c:/windows/temp folder has less than 60,000 files",
                    "text": "Ensure c:/windows/temp folder has less than 60,000 files"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
            "required": true
        },
        {
            "id": "error_message",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "Provide the error message that are you seeing:",
            "watermarkText": "Copy and paste error message text from the console",
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
