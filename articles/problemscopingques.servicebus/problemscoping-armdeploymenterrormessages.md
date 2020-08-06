<properties
pageTitle="ARM template deployment Failed"
description="Issues where ARM APIs or ARM template deployments are failing"
service="microsoft.servicebus"
resource="errorMessageTypes"
authors="mksuni"
ms.author="mksuni"
displayOrder=""
selfHelpType="problemScopingQuestions"
supportTopicIds="32633393"
resourceTags=""
productPesIds="13186"
cloudEnvironments="public, Fairfax, usnat, ussec"
articleId="sb-arm-deployment-failures"
schemaVersion="1"
	ownershipId="AzureMessaging_Common"
/>
# Issues where ARM APIs or ARM template deployments are failing
---
{
    "subscriptionRequired": true,
    "title": "Issues where ARM APIs or ARM template deployments are failing",
    "fileAttachmentHint": "Please upload any browser developer tools trace or unencrypted fiddler trace of the problem.",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_issueFrequency",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "How frequently does the issue occur?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Always",
                    "text": "Always"
                },
                {
                    "value": "Intermittent",
                    "text": "Intermittent"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Didn't notice any trend"
                }
            ]
        },
        {
            "id": "problem_errorMessageText",
            "order": 3,
            "controlType": "multilinetextbox",
            "displayLabel": "Please provide the exact error message including Correlation ID , Tracking Id and timestamp, if any",
            "required": true,
            "useAsAdditionalDetails": true
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Details",
            "watermarkText": "Provide additional information about your issue",
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