<properties
                pageTitle="Networking/Network Policy"
                description="Networking/Network Policy"
                authors="ChiragPavecha"
                ms.author="chiragpa"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32637207"
                productPesIds="16450"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="problemscoping-networking-network-policy"
	ownershipId="Compute_AzureKubernetesService"
/>
# Network Policy
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Cluster failed state",
    "fileAttachmentHint": "Attach the output of **kubectl get networkpolicies -o yaml**",
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
            "id": "getNetworkPolicyProvider",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Which network policy provider you are using?",
            "infoBalloonText": "Read <a href='https://docs.microsoft.com/azure/aks/use-network-policies#differences-between-azure-and-calico-policies-and-their-capabilities'>here</a> for AKS supported policy providers.",
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
