<properties
pageTitle="Other Issues"
description="Other Issues"
service="microsoft.containerregistry"
authors="nathana1"
ms.author="nathana"
selfHelpType="problemScopingQuestions"
supportTopicIds="32680725,32680695,32680726"
productPesIds="16213"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="problemscoping-generic"
schemaVersion="1"
	ownershipId="ContainerRegistry_Runtime"
/>
# Other Issues
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Other Issues",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "required": true,
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