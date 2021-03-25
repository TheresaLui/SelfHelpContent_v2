<properties
	pageTitle="Portal and UI/Portal page or blade errors"
	description="Portal and UI/Portal page or blade errors"
	authors="genlin"
	ms.author="kawilson"
    selfHelpType="problemScopingQuestions"
	supportTopicIds="32749427"
    productPesIds="15947"
	cloudEnvironments="public, blackForest, mooncake, fairfax, usnat, ussec"
    articleId="b1b6273d-908e-4f2d-2511-36a830ea0107"
	schemaVersion="1"
	ownershipId="Azure_Security_Security_Center"
/>
# Portal and UI/Portal page or blade errors
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Portal and UI/Portal page or blade errors",
    "fileAttachmentHint": "Please upload the network capture log (HAR file) or a file that may help diagnose the issue.",
    "formElements": [
        {
            "id": "RBAC_role",
            "order": 1,
            "controlType": "textbox",
            "displayLabel": "What Azure RBAC roles are assigned to your account?",
            "watermarkText": "Example: Virtual Machine Contributor",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 2,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "",
            "useAsAdditionalDetails": true,
            "required": true,
            "hints": [
                {
                    "text": "To capture the browser network trace, see <a href='https://docs.microsoft.com/azure/azure-portal/capture-browser-trace'>this document</a>."
                }
            ]
        },
        {
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": false
        }
    ],
    "$schema": "SelfHelpContent"
}
---
