<properties
                pageTitle="ClusterManagement/Performance high CPU or high Memory"
                description="Performance high CPU or high Memory"
                authors="ChiragPavecha"
                ms.author="chiragpa"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32683758"
                productPesIds="16450"
                cloudEnvironments="Public,Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="problemscoping-cluster-management-performance-high-cpu-memory"
	ownershipId="Compute_AzureKubernetesService"
/>
# Performance high CPU or high Memory
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Performance",
    "fileAttachmentHint": "Output of **kubectl top nodes** and **kubectl top pods --all-namespaces** would be helpful with the investigation",
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
            "id": "getExpectedBehavior",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "What's the expected performance?",
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
