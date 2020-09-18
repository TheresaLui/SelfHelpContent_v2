<properties
                pageTitle="Cluster Management/NotReady state"
                description="Cluster Management/NotReady state"
                authors="ChiragPavecha"
                ms.author="chiragpa"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32637196"
                productPesIds="16450"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="problemscoping-cluster-management-notready-state"
	ownershipId="Compute_AzureKubernetesService"
/>
# Cluster NotReady state
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Cluster NotReady state",
    "fileAttachmentHint": "Attach the output of **kubectl describe nodes** and **kubectl get nodes -o wide**",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
