
<properties
    articleId="problemscopingques-Create_or_delete_workspace"
    pageTitle="Create or delete workspace"
    description="Create or delete workspace"
    authors="yossiy,neilghuman"
    ms.author="yossiy,neghuman"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32612513"
    productPesIds="15725"
    cloudEnvironments="Public, Fairfax, usnat, ussec"
    schemaVersion="1"
    ownershipId="AzureMonitoring_LogAnalytics"
/>

# Create or delete workspace
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Create or delete workspace",
    "fileAttachmentHint": "Please provide a screenshot of any errors. In case you’re using an ARM template, please compress all the relevant JSON files and upload the ZIP file.",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start happening?",
            "required": true
        },
                {
            "id": "operation",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Which operation are you trying to perform?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Create a new workspace",
                    "text": "Create a new workspace"
                },
                {
                    "value": "Recover a soft-deleted workspace",
                    "text": "Recover a soft-deleted workspace"
                },
                {
                    "value": "Delete a workspace",
                    "text": "Delete a workspace"
                },
                                {
                    "value": "Permanently delete a workspace",
                    "text": "Permanently delete a workspace"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Not sure"
                }
            ],
            "required": true
        },
        {
            "id": "users",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Is the issue happening with a single user or multiple users?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Single user",
                    "text": "Single user"
                },
                {
                    "value": "Multiple users",
                    "text": "Multiple users"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Not sure"
                }
            ],
            "required": true
        },
        {
            "id": "interface",
            "order": 7,
            "controlType": "dropdown",
            "displayLabel": "Which user experience are you using?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Azure portal",
                    "text": "Azure portal"
                },
                {
                    "value": "Azure PowerShell",
                    "text": "Azure PowerShell"
                },
                {
                    "value": "Azure CLI",
                    "text": "Azure CLI"
                },
                {
                    "value": "Azure REST API",
                    "text": "Azure REST API"
                },
                {
                    "value": "Azure Resource Manager (ARM) template",
                    "text": "Azure Resource Manager (ARM) template"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other"
                }
            ],
            "required": true
        },
        {
            "id": "problem_description",
            "order": 9,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Describe the issue, including as much detail as possible with the exact text of error messages where available. If using an experience other than Azure portal, provide the commands being executed or the API call being made.",
            "required": true,
            "hints": []
        }
    ],
    "$schema": "SelfHelpContent"
}
---