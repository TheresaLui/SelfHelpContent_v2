<properties
	pageTitle="Portal and UI/Inventory in security center"
	description="Portal and UI/Inventory in security center"
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
# Portal and UI/Inventory in security center
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Portal and UI/Inventory in security center",
    "fileAttachmentHint": "",
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
             "infoBalloonText": "To capture the network log, see <a href='https://docs.microsoft.com/azure/azure-portal/capture-browser-trace'>this document</a>",
            "displayLabel": "Description",
            "watermarkText": "Please upload the network capture log (HAR file) by using the file load option",
            "useAsAdditionalDetails": true,
            "required": true
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
