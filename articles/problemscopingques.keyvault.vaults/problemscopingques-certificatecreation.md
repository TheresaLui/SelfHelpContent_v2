<properties
         pageTitle="General scoping question for Key Vault support requests."
         description="General scoping question for Key Vault support requests."
         authors="osmuller"
         ms.author="osmuller"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32739895"
         productPesIds="15657"
         schemaVersion="1"
         articleId="problemscopingques-certificatecreation"
	     cloudEnvironments="blackForest, fairfax, public, MoonCake, usnat, ussec"
	     ownershipId="AzureKeyVault_KeyVault"
/>
# Vault cannot be found
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
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
            "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Provide additional information about your issue including any error messages you are seeing.",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "creation_method",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "What method of certificate creation was used?",
            "dropdownOptions": [{
                    "value": "Powershell",
                    "text": "Powershell"
                }, {
                    "value": "CLI",
                    "text": "CLI"
                },{
                    "value": "Portal",
                    "text": "Portal"
                },{
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": true
        },
        {
            "id": "other_creation_method",
            "visibility": "creation_method == Other",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Creation Method",
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
