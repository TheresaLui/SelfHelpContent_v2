<properties
                pageTitle="Cluster Management/addon"
                description="Cluster Management/addon"
                authors="ChiragPavecha"
                ms.author="chiragpa"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32637177"
                productPesIds="16450"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="problemscoping-cluster-management-addon"
	ownershipId="Compute_AzureKubernetesService"
/>
# AddOn related issues
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "AddOn related issues",
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
            "id": "getAddOnDetails",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Select an AddOn you have problem with",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "OMS Agent",
                    "text": "OMS Agent"
                },
                {
                    "value": "Virtual Kubelet",
                    "text": "Virtual Kubelet"
                },
                {
                    "value": "Http Application Routing",
                    "text": "Http Application Routing"
                },
                {
                    "value": "Container Insight",
                    "text": "Container Insight"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other"
                }
            ],
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
