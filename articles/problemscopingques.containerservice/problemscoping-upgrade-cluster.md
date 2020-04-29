<properties
                pageTitle="problem during cluster upgrade"
                description="problem during cluster upgrade"
                authors="ChiragPavecha"
                ms.author="chiragpa"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32637185"
                productPesIds="16450"
                cloudEnvironments="Public, Fairfax, usnat, ussec"
                schemaVersion="1"
                articleId="b2ecdb4d-ff62-4ed2-9a20-29ca8b399640"
	ownershipId="Compute_AzureKubernetesService"
/>
# Cluster upgrade
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
    "title": "Cluster upgrade",
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
            "id": "getUpgradeVersion",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "What version of Kubernetes are you upgrading From and To?",
            "watermarkText": "For e.g. - From 1.x.y To 1.a.b",
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
