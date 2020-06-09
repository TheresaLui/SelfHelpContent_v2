<properties
                pageTitle="Identity/Authentication with ACR"
                description="Identity/Authentication with ACR"
                authors="ChiragPavecha"
                ms.author="chiragpa"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32637180"
                productPesIds="16450"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="problemscoping-identity-authentication-acr"
	ownershipId="Compute_AzureKubernetesService"
/>
# Authentication with ACR related
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Authentication with ACR related",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
        {
            "id": "getErrorMsg",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "What error message did you receive while performing this operation, if any?",
            "required": false
        },
        {
            "id": "getAuthenticationMode",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "What method of authentication are you using?",
            "watermarkText": "Choose an option",
            "infoBalloonText": "Read <a href='https://docs.microsoft.com/azure/container-registry/container-registry-auth-aks'>here</a> for authentication with ACR.",
            "dropdownOptions": [
                {
                    "value": "Service Principal",
                    "text": "Service Principal"
                },
                {
                    "value": "Kubernetes Secrets",
                    "text": "Kubernetes Secrets"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I don't know"
                }
            ],
            "required": false
        },
        {
            "id": "getACRRegistryAccess",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Are you able to access the ACR registry from a normal docker login?",
            "infoBalloonText": "Read <a href='https://docs.microsoft.com/azure/container-registry/container-registry-authentication#individual-login-with-azure-ad'>here</a> on how to do this.",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I don't try"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
