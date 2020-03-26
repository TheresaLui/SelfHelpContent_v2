<properties
pageTitle="Quota Issues"
description="Quota Issues"
service="microsoft.servicebus"
resource="quotaChangeRequest"
authors="mksuni"
ms.author="mksuni"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32633390"
resourceTags=""
productPesIds="13186"
cloudEnvironments="public, Fairfax"
articleId="sb-quota-request"
schemaVersion="1"
	ownershipId="AzureMessaging_Common"
/>
# Quota Issues
---
{
    "subscriptionRequired": true,
    "title": "Quota Issues",
    "fileAttachmentHint": "",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_QuotaChange",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "What quota increase are you requesting for?",
            "required": false
        },
        {
            "id": "problem_Reason",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Enter your justification for increase the quota",
            "watermarkText": "Provide your reasoning for quota change request",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Provide additional information about your issue",
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
