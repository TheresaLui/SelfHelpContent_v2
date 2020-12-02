<properties
         pageTitle="Scoping question for vault not found."
         description="Scoping question for vault not found."
         authors="osmuller"
         ms.author="osmuller"
         selfHelpType="problemScopingQuestions"
         supportTopicIds="32375295,32452742,32738117"
         productPesIds="15657"
         schemaVersion="1"
         articleId="problemscopingques-cannotfindvault"
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
        "description": "OurKey Vault Troubleshooter can help you troubleshoot and solve your problem.",
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
            "id": "vault_name",
            "order": 2,
            "visibility": "null",
            "controlType": "textbox",
            "displayLabel": "Vault name",
            "watermarkText": "E.g. MyContosoVault",
            "required": true,
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
        }
    ],
    "$schema": "SelfHelpContent"
}
---
