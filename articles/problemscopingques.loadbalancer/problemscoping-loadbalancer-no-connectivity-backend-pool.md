<properties
                pageTitle="Networking/No connectivity to backend pool"
                description="Networking/No connectivity to backend pool"
                authors="genlin"
                ms.author="genli"
                selfHelpType="problemScopingQuestions"
                supportTopicIds="32588977"
                productPesIds="16098"
                cloudEnvironments="Public"
                schemaVersion="1"
                articleId="c515f682-dcdb-4ad4-a075-230804ca2aa2"
/>
# No connectivity to backend pool
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "No connectivity to backend pool",
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
            "id": "is_backend_issue",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Can you access the backend pool instance directly without the load balancer?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes."
                },
                {
                    "value": "No",
                    "text": "No, it timeouts"
                },
                {
                    "value": "dont_know_answer",
                    "text": "I didn't try"
                }
            ],
            "required": false
        },
        {
            "id": "info_backendissue",
            "order": 3,
            "visibility": "is_backend_issue == Yes",
            "controlType": "textbox",
            "displayLabel": "Tips",
           "watermarkText": "If you cannot access backend pool instance directly, this issue should not be considered as a load balancer issue. Please try to fix the connectivity issue with the backend pool instance first.",
            "required": false
        },
        {
            "id": "problem_description",
            "order": 4,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "useAsAdditionalDetails": true,
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
