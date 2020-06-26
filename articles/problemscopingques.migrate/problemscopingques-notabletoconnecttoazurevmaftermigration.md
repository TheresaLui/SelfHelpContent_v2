<properties
         pageTitle="Scoping questions for not able to connect to the Azure VM after migration"
         description="Scoping questions for not able to connect to the Azure VM after migration"
         authors="An-mol"
         ms.author="anvar"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32675756"
         productPesIds="16348"
         cloudEnvironments="public, Fairfax, usnat, ussec"
         schemaVersion="1"
        articleId="ddb7ef68-ca90-4454-a6eb-0f04e8e2761d"
	ownershipId="Compute_AzureMigrate"
/>

# Not able to connect to the Azure VM after migration

---
{
    "subscriptionRequired": false,
    "resourceRequired": false,
    "title": "Not able to connect to the Azure VM after migration",
    "fileAttachmentHint": "",
    "formElements": [
{
            "id": "server_kind",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "What kind of servers are you trying to replicate?",
            "watermarkText": "Select",
            "dropdownOptions": [
                {
                    "value": "VMware VMs",
                    "text": "VMwareVMs"
                },
                {
                    "value": "Hyper-V VMs",
                    "text": "Hyper-V VMs"
                },
                {
                    "value": "Physical Server",
                    "text": "Physical Server"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other"
                }
            ],
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 3,
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
