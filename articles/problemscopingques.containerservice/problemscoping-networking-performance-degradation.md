<properties
                pageTitle="Networking/Performance degradation"
                description="Networking/Performance degradation"
                authors="ChiragPavecha"
                ms.author="chiragpa"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32683759"
                productPesIds="16450"
                cloudEnvironments="Public,Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="problemscoping-networking-performance-degradation"
	ownershipId="Compute_AzureKubernetesService"
/>
# Performance Degradation
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Performance degradation",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When was the last time you experienced this issue?",
            "required": true
        },
        {
            "id": "getHowToMonitorPerf",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "How are you monitoring the Performance issue? If using any tool, please specify",
            "required": false
        },
        {
            "id": "getNetworkingModel",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Choose the networking model of your cluster",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "azurecni",
                    "text": "Azure CNI Networking"
                },
                {
                    "value": "kubenet",
                    "text": "Kubenet Networking"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I am not sure"
                }
            ],
            "infoBalloonText": "How to select appropriate <a href='https://docs.microsoft.com/azure/aks/operator-best-practices-network#choose-the-appropriate-network-model'>Networking model</a> for your AKS cluster.",
            "required": false
        },
        {
            "id": "getExpectedBehavior",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "What's the expected performance/latency?",
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
