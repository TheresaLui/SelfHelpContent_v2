<properties
         pageTitle="TSG questions for ASC"
         description="Troubleshooter questions with radio button"
         authors="akankshajsh"
         ms.author="akjoshi"
         selfHelpType="TSG_Questions"
         productPesIds="15922"
         cloudEnvironments="public"
         schemaVersion="1"
         articleId="tsg-questions-for-application-gateway"
/>
# TSG Questions for application gateway
---
{
    "title": "TSG questions for ASC",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "Approximate start time of the most recent occurrence",
            "required": true
        },
        {
            "id": "radio-button-example",
            "order": 2,
            "controlType": "radioButtonGroup",
            "displayLabel": "Select the error:",
            "radioButtonOptions": [
                {
                    "value": "Error_123",
                    "text": "Error 123"
                },
                {
                    "value": "Error_500",
                    "text": "Error 500"
                }
            ],
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
