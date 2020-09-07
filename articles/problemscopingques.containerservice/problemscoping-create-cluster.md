<properties
                pageTitle="Problem with cluster creation"
                description="Problem with cluster creation"
                authors="ChiragPavecha"
                ms.author="chiragpa"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32637190"
                productPesIds="16450"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="4a4301a5-9144-4c93-b482-f225df855dd0"
	ownershipId="Compute_AzureKubernetesService"
/>
# Cluster creation
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Cluster creation",
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
            "id": "getHowPerform",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "From where you are performing this operation?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Azure Portal",
                    "text": "Azure Portal"
                },
                {
                    "value": "CLI",
                    "text": "CLI"
                },
                {
                    "value": "Power Shell",
                    "text": "Power Shell"
                },
                {
                    "value": "Cloud Shell",
                    "text": "Cloud Shell"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I don't know"
                }
            ],
            "required": false
        },
        {
            "id": "getCloudShellCheck",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Does this operation fail through Cloud Shell as well?",
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
                    "text": "I didn't try"
                }
            ],
            "infoBalloonText": "You can avoid common local CLI issues by using <a href='https://docs.microsoft.com/azure/cloud-shell/overview'>Azure Cloud Shell</a>.",
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
