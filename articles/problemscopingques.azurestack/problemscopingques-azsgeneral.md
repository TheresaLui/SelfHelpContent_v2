<properties
    pageTitle="Azure Stack Environment Details"
    description="Additional details for on-premises Azure Stack issue"
    authors="alexsmithMSFT"
    authorAlias="alexsmit"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32567908,32567920,32567910,32591343,32567944,32591348,32591349,32629171,32629199,32629201,32629220,32629221,32629224,32629229,32629237,32629241,32629256,32629262,32629266,32629267,32629180,32629195,32629240,32629271,32629272"
    productPesIds="16226"
    cloudEnvironments="public"
    schemaVersion="1"
    articleId="8ccb2fde-6f9f-4e97-b700-4b07ac45db50"
/>
# Azure Stack Environment Details
---
{
    "resourceRequired": false,
    "title": "Azure Stack Environment Details",
    "fileAttachmentHint": "To help the support agent identify your issue, please collect and upload the output of Test-AzureStack, Get-AzureStackStampInformation, and/or Azure Stack seed ring logs by following the steps to <a href='https://docs.microsoft.com/azure/azure-stack/azure-stack-diagnostic-test'>Run a validation test for Azure Stack</a>",
    "formElements": [{
            "id": "hardware_partner",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Azure Stack hardware partner",
            "watermarkText": "Azure Stack OEM Name",
            "dropdownOptions": [{
                    "value": "Avanade",
                    "text": "Avanade"
                },{
                    "value": "Cisco",
                    "text": "Cisco"
                },{
                    "value": "Dell-EMC",
                    "text": "Dell-EMC"
                },{
                    "value": "Fujitsu",
                    "text": "Fujitsu"
                },{
                    "value": "HPE",
                    "text": "HPE"
                },{
                    "value": "Huawei",
                    "text": "Huawei"
                },{
                    "value": "Lenovo",
                    "text": "Lenovo"
                },{
                    "value": "Terra",
                    "text": "Terra"
                },{
                    "value": "Other",
                    "text": "Other"
                }
                ],
            "required": false,
            "infoBalloonText": "Choose the partner or OEM for the hardware your Azure Stack stamp is running on"
        },{
            "id": "patch_level",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Current Patch Level",
            "watermarkText": "Example: 1807 if your build number is 1.1807.0.76.",
            "dropdownOptions": [{
                    "value": "1811",
                    "text": "1811"
                },{
                    "value": "1810",
                    "text": "1810"
                },{
                    "value": "1809",
                    "text": "1809"
                },{
                    "value": "1808",
                    "text": "1808"
                },{
                    "value": "1807",
                    "text": "1807"
                },{
                    "value": "1805",
                    "text": "1805"
                },{
                    "value": "Pre-1805",
                    "text": "Pre-1805"
                },{
                    "value": "Other",
                    "text": "Other"
                }
                ],
            "required": false,
            "infoBalloonText": "Example: Select 1807 if your build number is 1.1807.0.76."
        },{
            "id": "region_name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Region Name",
            "watermarkText": "Name of your Azure Stack region",
            "required": false,
            "infoBalloonText": "If you have more than one Azure Stack environment, Ex: REGION from https://adminportal.REGION.FQDN"
        },{
            "id": "problem_start_time",
            "order": 4,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },{
            "id": "problem_description",
            "order": 5,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "useAsAdditionalDetails": true,
            "required": true
        }
    ]
}
---