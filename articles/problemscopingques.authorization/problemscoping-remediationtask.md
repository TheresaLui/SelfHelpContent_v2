<properties
    pageTitle="Remediation task behavior not as expected"
    description="Remediation task behavior not as expected"
    service="microsoft.authorization"
    resource="remediations"
    authors="kenieva"
    ms.author="kenieva"
    displayOrder=""
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32741672"
    resourceTags=""
    productPesIds="16456"
    cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
    articleId="1d0baad2-c201-4369-9513-233dfa2b6b6c"
    schemaVersion="1"
    ownershipId="Compute_AzurePolicy"
/>
# Remediation task behavior not as expected
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Policy Remediation Task",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 10,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "remediationTaskId",
            "order": 20,
            "controlType": "dropdown",
            "displayLabel": "Please select the remediation task.",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionId}/providers/Microsoft.PolicyInsights/remediations?api-version=2019-07-01",
                "jTokenPath": "value",
                "textProperty": "name",
                "textTemplate": "{name}",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            },
            "DropdownOptions": [
                {
                    "value": "NoRemediationTask",
                    "text": "Unable to retrieve list of policy remediation task"
                }
            ],
            "required": true
        },
        {
            "id": "problem_description",
            "order": 50,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Provide additional information about the issue and what is your expectation",
            "required": true,
            "useAsAdditionalDetails": true,
            "hints": [
                {
                    "text": "Issue description."
                }
            ]
        }
    ],
    "$schema": "SelfHelpContent"
}
---
