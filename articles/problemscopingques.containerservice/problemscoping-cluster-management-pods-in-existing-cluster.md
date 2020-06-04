<properties
                pageTitle="Cluster Management/Problem with Pods in existing cluster"
                description="Cluster Management/Problem with Pods in existing cluster"
                authors="ChiragPavecha"
                ms.author="chiragpa"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32683762"
                productPesIds="16450"
                cloudEnvironments="Public,Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="problemscoping-cluster-management-pods-in-existing-cluster"
	ownershipId="Compute_AzureKubernetesService"
/>
# Problem with Pods in existing cluster
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Problem with Pods",
    "fileAttachmentHint": "Output of **kubectl get pods -o wide** and **kubectl describe pod yourpodname** would be helpful with the investigation",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When was the last time you experienced this issue?",
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
            "id": "getPodName",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Mention the Pod name you have problem with, if known",
            "required": false
        },
        {
            "id": "getPortSettings",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Have you configured the required port for AKS cluster?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "infoBalloonText": "Check the list of <a href='https://docs.microsoft.com/azure/aks/limit-egress-traffic#required-ports-and-addresses-for-aks-clusters'>required ports</a> for AKS cluster.",
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
