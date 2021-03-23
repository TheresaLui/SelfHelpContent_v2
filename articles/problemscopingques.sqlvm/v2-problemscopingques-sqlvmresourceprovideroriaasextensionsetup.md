<properties 
  pageTitle="SQL Virtual Machine Resource or IaaS Extension setup"
  description="SQL Virtual Machine Resource or IaaS Extension setup"
  authors="ujpat,amamun"
  ms.author="ujpat,amamun"
  selfHelpType="problemScopingQuestions"
  supportTopicIds="32740102"
  productPesIds="14745"
  cloudEnvironments="Public, BlackForest, Fairfax, Mooncake, USSEC, USNAT"
  schemaVersion="1"
  articleId="fbb02313-b08e-467f-a1ca-974d66641e59"
  ownershipId="AzureData_AzureSQLVM"
/>
# SQL Virtual Machine Resource or IaaS Extension setup
---
{
    "resourceRequired": false,
    "subscriptionRequired": false,
    "title": "SQL Virtual Machine Resource or IaaS Extension setup",
    "fileAttachmentHint": null,
     "diagnosticCard": {
    "title": "SQL Virtual Machine Resource or IaaS Extension setup Troubleshooter",
    "description": "Our SQL Virtual Machine Resource or IaaS Extension setup Troubleshooter can help you troubleshoot and solve your problem.",
    "insightNotAvailableText": "Our troubleshooter did not detect any issues with your resource. See our manual troubleshooting steps below to troubleshoot your problem."
  },
    "formElements": [
        {
            "id": "problem_start_time",
            "order": 1,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start",
            "required": false
        },
        {
            "id": "how_setup",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "What assistance you are looking for",
            "watermarkText": "Choose an option",
            "dropdownOptions": [
                {
                    "text": "Install/Remove SQL IaaS Extension",
                    "value": "Install_Remove"
                },
                {
                    "text": "Errors encountered using IaaS Extension",
                    "value": "Error_Encountered"
                },
                {
                    "text": "Configure/Managing the SQL VM Resource features",
                    "value": "Configure_Manage_RP"
                },
                {
                    "text": "I'm not sure/don't know",
                    "value": "dont_know_answer"
                }
            ],
            "required": true
        },
        {
            "id": "customer_consent",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Choose yes to display dynamic insights.",
            "watermarkText": "Dynamic Insights",
            "infoBalloonText": "Dynamic Insights",
            "dropdownOptions": [
            {
            "value": "yes",
            "text": "Yes"
            },
            {
            "value": "no",
            "text": "No"
            }
        ],
            "required": true,
            "diagnosticInputRequiredClients": "Portal"
        }
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
