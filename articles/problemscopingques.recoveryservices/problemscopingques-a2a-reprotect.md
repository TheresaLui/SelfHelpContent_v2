<properties
         pageTitle="Scoping questions for Azure VM re-protection"
         description="Scoping questions for Azure VM re-protection"
         authors="genlin"
         ms.author="asgang"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32574723"
         productPesIds="16370"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
         articleId="2b342a85-2011-4b4d-2220-43639892e013"
	ownershipId="Compute_SiteRecovery"
/>
# Questions Azure VM re-protection Failures
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Azure VM re-protection failures",
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
            "displayLabel": "Enter the ID of failed Site Recovery job Activity ID:",
            "watermarkText": "Example: cace7461-dd3c-4e38-b4db-38dc57fdee7b",
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
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
        }
    ],
    "$schema": "SelfHelpContent"
}
---
