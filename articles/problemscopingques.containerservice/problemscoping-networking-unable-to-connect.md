<properties
                pageTitle="Networking/Unable to connect to the cluster"
                description="Networking/Unable to connect to the cluster"
                authors="ChiragPavecha"
                ms.author="chiragpa"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32637189"
                productPesIds="16450"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="problemscoping-networking-unable-to-connect"
	ownershipId="Compute_AzureKubernetesService"
/>
# Unable to connect to the cluster
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Cluster failed state",
    "fileAttachmentHint": "Attach the output of **kubectl get pods -n kube-system**",
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
            "id": "getCommandStatus",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Are you able to run 'kubectl logs' or 'kubectl exec' commands?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "timeout",
                    "text": "No, it timeouts"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I didn't try"
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
