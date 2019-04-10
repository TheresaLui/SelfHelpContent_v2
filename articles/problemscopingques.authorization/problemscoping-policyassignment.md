<properties
    pageTitle="Policy behavior not as expected"
    description="Policy behavior not as expected"
    service="microsoft.authorization"
    resource="policyAssignments"
    authors="robga"
    ms.author="robga"
    displayOrder=""
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32636046,32636050"
    resourceTags=""
    productPesIds="16456"
    cloudEnvironments="public"
    articleId="1d0baad2-c201-4369-9513-233dfa2b6b6b"
    schemaVersion="1"
/>
#Policy behavior not as expected
---
{
    "subscriptionRequired": true,
    "title": "Policy definition",
    "fileAttachmentHint": "",
    "formElements":
    [
        {
            "id": "policyDefinition",
            "order": 10,
            "controlType": "dropdown",
            "displayLabel": "Please provide the policy definition",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/providers/Microsoft.Authorization/policyDefinitions?api-version=2019-01-01",
                "jTokenPath": "value",
                "textProperty": "properties.displayName,name",
                "textTemplate": "{properties.displayName}  ({name})",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            },
            "DropdownOptions": [
                {
                    "value": "NoPolicyDefinition",
                    "text": "Unable to retrieve list of policy definition"
                }
            ],
            "required": true
        },
        {
            "id": "policyAssignment",
            "order": 20,
            "controlType": "dropdown",
            "displayLabel": "Please provide the policy assignment",
            "dynamicDropdownOptions": {
                "uri": "/subscriptions/{subscriptionid}/providers/Microsoft.Authorization/policyAssignments?api-version=2019-01-01&$filter=atScope()",
                "jTokenPath": "value",
                "textProperty": "properties.displayName,name",
                "textTemplate": "{properties.displayName}  ({name})",
                "valueProperty": "id",
                "textPropertyRegex": "[^/]+$",
                "defaultDropdownOptions": {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            },
            "DropdownOptions": [
                {
                    "value": "NoPolicyAssignment",
                    "text": "Unable to retrieve list of policy assignment"
                }
            ],
            "required": true
        }
    ]
}
---