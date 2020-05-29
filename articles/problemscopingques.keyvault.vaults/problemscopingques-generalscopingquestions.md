<properties
         pageTitle="General scoping question for Key Vault support requests."
         description="General scoping question for Key Vault support requests."
         authors="osmuller"
         ms.author="osmuller"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32739887,32739888,32739889,32739890,32739891,32739892,32739893,32738119,32375289,32375296,32375297,32738115,32375295,32596890,32596891,32375283,32375284,32375287,32375288,32375291,32738120,32452742,32739895,32739896,32738118,32596889,32596882,32596884,32375292,32375293,32738117,32739894,32596886,32738116,32596879,32596880,32596881,32596883,32375294"
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
            "controlType": "multilinetextbox",
            "displayLabel": "What is the expected experience and how does that differ from the actual result?",
            "required": false,
            "useAsAdditionalDetails": true,
            "required": true
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
                    "text": "Yes"
                }, {
                    "value": "no",
                    "text": "No"
                }
            ],
            "required": true
        },
        {
            "id": "application_environment",
            "order": 5,
            "controlType": "multiselectdropdown",
            "displayLabel": "Select the environments that are running your applications",
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
            "required": true
        },
        {
            "id": "other_application_environment",
            "visibility": "application_environment == Other",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "Application Environment",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
