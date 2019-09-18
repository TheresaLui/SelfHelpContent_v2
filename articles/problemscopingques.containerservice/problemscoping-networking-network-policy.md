<properties
                pageTitle="Networking/Network Policy"
                description="Networking/Network Policy"
                authors="ChiragPavecha"
                ms.author="chiragpa"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32637207"
                productPesIds="16450"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="problemscoping-networking-network-policy"
/>
# Network Policy
---
{
    "subscriptionRequired": true,
    "resourceRequired": no,
    "title": "Cluster failed state",
    "fileAttachmentHint": "Attach the output of **kubectl get networkpolicies -o yaml**",
    "formElements": [
           {
            "id": "is_backend_issue",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Can you access the backend pool instance directly without the load balancer?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes. "
                },
                {
                    "value": "No",
                    "text": "No, it timeouts. Tips: In this case you need to fix the connectivity issue with the backed pool instance first. The issue should not be considered as a load balancer issue"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I didn't try"
                }
            ],
            "required": false
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
        {
            "id": "getErrorMsg",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "What error message did you receive while performing this operation, if any?",
            "required": false
        },
        {
            "id": "getNetworkPolicyProvider",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Which network policy provider you are using?",
            "infoBalloonText": "Read <a href='https://docs.microsoft.com/azure/aks/use-network-policies#differences-between-azure-and-calico-policies-and-their-capabilities'>here</a> for AKS supported policy providers.",
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
