<properties
    pageTitle="Azure Stack Environment Details"
    description="Additional details for on-premises Azure Stack issue"
    authors="alexsmithMSFT"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32567908,32567920"
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
    "fileAttachmentHint": "To help the support agent identify your issue, collect and upload the output of Test-AzureStack, Get-AzureStackStampInformation, and Azure Stack seed ring logs according to the article: <a href='https://docs.microsoft.com/azure/azure-stack/azure-stack-diagnostic-test'>Run a validation test for Azure Stack</a>",
    "formElements": [{
            "id": "hardware_partner",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Azure Stack hardware partner",
            "watermarkText": "Choose a partner name",
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
            "required": false
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
            "hints": [{
                    "text": "Example: 1807 if your build number is 1.1807.0.76."
                }]
        },{
            "id": "region_name",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Region Name",
            "watermarkText": "Name of your Azure Stack region",
            "required": false,
            "hints": [{
                    "text": "If you have more than one Azure Stack environment, Ex: REGION from https://adminportal.REGION.FQDN"
                }]
        }
    ]
}
---