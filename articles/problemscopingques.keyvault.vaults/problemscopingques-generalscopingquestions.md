<properties
         pageTitle="General scoping question for Key Vault support requests."
         description="General scoping question for Key Vault support requests."
         authors="osmuller"
         ms.author="osmuller"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32375295,32596891,32452742,32738117,32738118,32738116"
         productPesIds="15657"
         schemaVersion="1"
         articleId="problemscopingques-generalscopingquestions"
	     cloudEnvironments="blackForest, fairfax, public, MoonCake, usnat, ussec"
	     ownershipId="AzureKeyVault_KeyVault"
/>
# Vault cannot be found
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Vault cannot be found",
    "fileAttachmentHint": "",
    "diagnosticCard": {
        "title": "Key Vault Troubleshooter",
        "description": "Our Key Vault Troubleshooter can help you troubleshoot and solve your problem.",
        "insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource. See our manual troubleshooting steps below to troubleshoot your problem."
    },
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "Incident time",
            "required": true
        },
        {
            "id": "expected_experience",
            "order": 2,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "What is the expected result/experience and how does that differ from the actual result",
            "required": false,
            "diagnosticInputRequiredClients": "Portal"
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Provide additional information about your issue including any error messages you are seeing.",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "attached_screenshots",
            "order": 4,
            "controlType": "radioButtonGroup",
            "displayLabel": "Are screenshots attached:",
            "radioButtonOptions": [{
                    "value": "yes",
                    "text": "yes"
                }, {
                    "value": "no",
                    "text": "no"
                }
            ],
            "required": true
        },
        {
            "id": "application_environment",
            "order": 5,
            "controlType": "multiselectdropdown",
            "displayLabel": "Select the applications running on your virtual machine",
            "dropdownOptions": [{
                    "value": "Virtual Machine",
                    "text": "Virtual Machine"
                }, {
                    "value": "Application Service",
                    "text": "Application Service"
                }, {
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
