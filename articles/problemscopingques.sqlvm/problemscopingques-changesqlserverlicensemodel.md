<properties 
    pageTitle="licensing/changing sql licensing model"
    description="licensing/changing sql licensing model"
    authors="vadeveka"
    ms.author="vadeveka"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32633500"
    productPesIds="14745"
    cloudEnvironments="public,fairfax"
    schemaVersion="1"
    articleId="FE334468-7880-47A2-A6B7-35CF78B47546"
	ownershipId="AzureData_AzureSQLVM"
/>
# licensing/changing sql licensing model
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "licensing/changing sql licensing model",
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start",
            "required": false
        },
        {
            "id": "how",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "How are you attempting to change the license type?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "text": "Azure Portal",
                    "value": "Azure Portal"
                },
                {
                    "text": "Azure PowerShell",
                    "value": "Azure PowerShell"
                },
                {
                    "text": "Azure CLI",
                    "value": "Azure CLI"
                },
                {
                    "text": "Other, don't know or not applicable",
                    "value": "dont_know_answer"
                }
            ],
            "required": false
        },
        {
            "id": "error",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Did you encounter any error while applying the change?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "text": "Yes (describe below)",
                    "value": "Yes"
                },
                {
                    "text": "No",
                    "value": "dont_know_answer"
                }
            ],
            "required": false
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "required": true,
            "useAsAdditionalDetails": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
