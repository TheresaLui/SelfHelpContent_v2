<properties
                pageTitle="Cluster Management/dashboard"
                description="Cluster Management/dashboard"
                authors="ChiragPavecha"
                ms.author="chiragpa"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32637195"
                productPesIds="16450"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="problemscoping-cluster-management-dashboard"
	ownershipId="Compute_AzureKubernetesService"
/>
# Dashboard related issues
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Cluster dashboard",
    "fileAttachmentHint": "Attach the output of **az --version**",
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
            "id": "getCloudShellCheck",
            "order": 3,
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
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
