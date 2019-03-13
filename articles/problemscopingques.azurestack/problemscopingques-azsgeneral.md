<properties
    pageTitle="Azure Stack Environment Details"
    description="Additional details for on-premises Azure Stack issue"
    authors="alexsmithMSFT"
    ms.author="alexsmit"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32629170,32629186,32629190,32629191,32629222,32629225,32629227,32629228,32629258,32629259,32629265,32629171,32630572,32629199,32629201,32630573,32629220,32629221,32629224,32629229,32629237,32629241,32629256,32630574,32629262,32629266,32629267,32629172,32629192,32629173,32629196,32629217,32629218,32629219,32629252,32629254,32629273,32629174,32629236,32629239,32629274,32629175,32629244,32629215,32629216,32629188,32630575,32629232,32629245,32629246,32629247,32630576,32629269,32629270,32629176,32629194,32629205,32629233,32629251,32629253,32629177,32629178,32629189,32629204,32629209,32629212,32629179,32629202,32629210,32629211,32629213,32629223,32629230,32629231,32629277,32629281,32629282,32629180,32629195,32629240,32630577,32629271,32629272,32629181,32629234,32629235,32629242,32629243,32629249,32629250,32629263,32629264,32629182,32629187,32629193,32629198,32629255,32629257,32629183,32629197,32629207,32629208,32629248,32629260,32629261,32629268,32629184,32629200,32629278,32629185,32629206,32629226,32630578,32629275,32629276,32629279,32629280"
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
            "watermarkText": "Example: 1901 if your build number is 1.1901.0.99.",
            "dropdownOptions": [{
                    "value": "1902",
                    "text": "1902"
                },{
                    "value": "1901",
                    "text": "1901"
                },{
                    "value": "1811",
                    "text": "1811"
                },{
                    "value": "1809",
                    "text": "1809"
                },{
                    "value": "1808",
                    "text": "1808"
                },{
                    "value": "Other",
                    "text": "Other"
                }
                ],
            "required": false,
            "infoBalloonText": "Example: Select 1901 if your build number is 1.1901.0.99."
        },{
            "id": "build_number",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Current Build Number",
            "watermarkText": "Example: 1.1901.0.99",
            "required": false,
            "infoBalloonText": "Includes hotfixes. See steps to <a href='https://docs.microsoft.com/azure/azure-stack/azure-stack-updates#determine-the-current-version'>Determine the Current Version</a>"
        },{
            "id": "region_name",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Region Name",
            "watermarkText": "Name of your Azure Stack region",
            "required": false,
            "infoBalloonText": "If you have more than one Azure Stack environment, Ex: REGION from https://adminportal.REGION.FQDN"
        },{
            "id": "tenant_impact",
            "order": 5,
            "controlType": "dropdown",
            "displayLabel": "Availability of running tenant applications impacted",
            "watermarkText": "Tenant impact",
            "dropdownOptions": [{
                    "value": "Yes",
                    "text": "Yes"
                },{
                    "value": "No",
                    "text": "No"
                }
                ],
            "required": false,
            "infoBalloonText": "Choose yes if availability of running tenant applications has been impacted"
        },{
            "id": "problem_start_time",
            "order": 900,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },{
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "useAsAdditionalDetails": true,
            "required": true
        }
    ]
}
---