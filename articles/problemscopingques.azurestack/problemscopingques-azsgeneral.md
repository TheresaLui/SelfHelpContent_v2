<properties
    pageTitle="Azure Stack Environment Details"
    description="Additional details for on-premises Azure Stack issue"
    authors="alexsmithMSFT"
    ms.author="alexsmit, mquian, v-miegge"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32629227,32629228,32629258,32629259,32629192,32663928,32663927,32663926,32629196,32629217,32629218,32629252,32629254,32629188,32629242,32629245,32629247,32629249,32630576,32629269,32629234,32629263,32629177,32629189,32629204,32629209,32629212,32629195,32630577,32629271,32629272,32663929,32663930,32629187,32629193,32663921,32663913,32663902,32663903,32663904,32663906,32663905,32629200,32629278,32630572,32630573,32629220,32629221,32629224,32629237,32629241,32629256,32629267,32629270,32629194,32629205,32663934,32629253,32629198,32689841,32689842,32689843,32689844,32689845,32689846,32689847,32689855,32689833,32689834,32689836,32689837,32689838,32689851,32689828,32689830,32689835,32689839,32689840,32689849,32689850,32689852,32689858,32689829,32689831,32689832,32689848,32689853,32689854,32689856,32689857"
    productPesIds="16226,16963"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="8ccb2fde-6f9f-4e97-b700-4b07ac45db50"
    ownershipId="StorageMediaEdge_AzureStack_Hub"
/>
# Azure Stack Environment Details
---
{
    "subscriptionRequired": true,
    "resourceRequired": false,
    "title": "Azure Stack Environment Details",
    "fileAttachmentHint": "To help the support agent identify your issue, please collect and upload the output of Test-AzureStack, Get-AzureStackStampInformation, and/or Azure Stack seed ring logs by following the steps to <a href='https://docs.microsoft.com/azure/azure-stack/azure-stack-diagnostic-test'>Run a validation test for Azure Stack</a>",
    "formElements": [
        {
            "id": "hardware_partner",
            "order": 1,
            "controlType": "dropdown",
            "displayLabel": "Azure Stack hardware partner",
            "watermarkText": "Azure Stack OEM Name",
            "dropdownOptions": [
                {
                    "value": "Avanade",
                    "text": "Avanade"
                },
                {
                    "value": "Cisco",
                    "text": "Cisco"
                },
                {
                    "value": "Dell-EMC",
                    "text": "Dell-EMC"
                },
                {
                    "value": "Fujitsu",
                    "text": "Fujitsu"
                },
                {
                    "value": "HPE",
                    "text": "HPE"
                },
                {
                    "value": "Huawei",
                    "text": "Huawei"
                },
                {
                    "value": "Lenovo",
                    "text": "Lenovo"
                },
                {
                    "value": "Terra",
                    "text": "Terra"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": false,
            "infoBalloonText": "Choose the partner or OEM for the hardware your Azure Stack stamp is running on"
        },
        {
            "id": "cloud_id",
            "order": 2,
            "controlType": "textbox",
            "displayLabel": "Enter the Stamp Cloud ID",
            "watermarkText": "########-####-####-####-###########",
            "infoBalloonText": "Learn how to <a href='https://docs.microsoft.com/azure-stack/operator/azure-stack-find-cloud-id'>find your Stamp Cloud ID. If you aren't sharing diagnostic data or you're running a build earlier than 1910, type N/A.</a>",
            "required": true
        },
        {
            "id": "patch_level",
            "order": 3,
            "controlType": "dropdown",
            "displayLabel": "Current Patch Level",
            "watermarkText": "Example: 2008 if your build number is 1.2008.0.35.",
            "dropdownOptions": [
{
                    "value": "2008",
                    "text": "2008"
                },
                {
                    "value": "2005",
                    "text": "2005"
                },
                {
                    "value": "2002",
                    "text": "2002"
                },
                {
                    "value": "1910",
                    "text": "1910"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": false,
            "infoBalloonText": "Example: Select 2008 if your build number is 1.2008.0.35."
        },
        {
            "id": "build_number",
            "order": 4,
            "controlType": "textbox",
            "displayLabel": "Current Build Number",
            "watermarkText": "Example: 1.2008.0.35",
            "required": false,
            "infoBalloonText": "Includes hotfixes. Learn how to <a href='https://docs.microsoft.com/azure-stack/operator/azure-stack-apply-updates#determine-the-current-version'>determine the current build number</a>"
        },
        {
            "id": "region_name",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Region Name",
            "watermarkText": "Name of your Azure Stack region",
            "required": false,
            "infoBalloonText": "If you have more than one Azure Stack environment, Ex: REGION from https://adminportal.REGION.FQDN"
        },
        {
            "id": "tenant_impact",
            "order": 6,
            "controlType": "dropdown",
            "displayLabel": "Availability of running tenant applications impacted",
            "watermarkText": "Tenant impact",
            "dropdownOptions": [
                {
                    "value": "Yes",
                    "text": "Yes"
                },
                {
                    "value": "No",
                    "text": "No"
                }
            ],
            "required": false,
            "infoBalloonText": "Choose yes if availability of running tenant applications has been impacted"
        },
        {
            "id": "problem_start_time",
            "order": 900,
            "controlType": "datetimepicker",
            "displayLabel": "When did the problem start?",
            "required": true
        },
        {
            "id": "problem_description",
            "order": 1000,
            "controlType": "multilinetextbox",
            "displayLabel": "Description",
            "watermarkText": "Provide additional information about your issue",
            "useAsAdditionalDetails": true,
            "required": true
        }
    ],
    "$schema": "SelfHelpContent"
}
---
