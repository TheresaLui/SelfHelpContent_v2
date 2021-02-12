<properties
    pageTitle="Scoping questions for count mismatch on Azure Migrate dashboard"
    description="Scoping questions for count mismatch on Azure Migrate dashboard"
    authors="An-mol"
    ms.author="anvar"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32675739, 32675738"
    productPesIds="16348"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="275455e6-9c0f-43fa-9459-b011230d20fd"
	ownershipId="Compute_AzureMigrate"
/>
# Count mismatch on Azure Migrate Dashboard
---
{
    "subscriptionRequired": true,
    "resourceRequired": true,
   "title": "Count mismatch on Azure Migrate dashboard",
    "fieAttachmentHint": "",
    "formElements": [
              {            "id": "countmismatch_metric",
           "order": 1,
           "visibility": "null",
           "controlType": "textbox",
            "displayLabel": "Which metric does not match?",
            "watermarkText": "E.g. Discovered Servers",
            "required": true
        },
        {
            "id": "problem_start_time",
            "order": 2,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem begin?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 3,
            "controlType": "multilinetextbox",
            "useAsAdditionalDetails": true,
            "displayLabel": "Additional details",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "hints": []
        }
    ],
    "$schema": "SelfHelpContent"
}
---
