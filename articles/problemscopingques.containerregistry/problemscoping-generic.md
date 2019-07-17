<properties
pageTitle="Other Issues"
description="Other Issues"
service="microsoft.containerregistry"
authors="nathana1"
ms.author="nathana"
selfHelpType="problemScopingQuestions"
supportTopicIds=""
productPesIds="16213"
cloudEnvironments="public"
articleId="problemscoping-generic"
schemaVersion="1"
/>
# Other Issues
---
{
    "subscriptionRequired": true,
    "title": "Other Issues",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?"
        },
        {
            "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Provide the exact command and error message with any addition details (such as the output from 'az acr check-health --name myregistry --ignore-errors --yes').",
            "required": true,
            "useAsAdditionalDetails": false,
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