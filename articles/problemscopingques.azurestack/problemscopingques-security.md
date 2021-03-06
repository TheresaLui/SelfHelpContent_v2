<properties
    pageTitle="Azure Stack Security, Secrets Management, and Identity"
    description="Azure Stack Security, Secrets Management, and Identity"
    authors="alexsmithMSFT"
    ms.author="alexsmit, mquian, v-miegge"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32663931,32663932,32629257"
    productPesIds="16226"
    ownershipId="StorageMediaEdge_AzureStack_Hub"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="8ccb2fde-4000-4e97-b711-4b07ac45db50"
/>
# Azure Stack Security, Secrets Management and Identity
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
            "infoBalloonText": "Find your <a href='https://docs.microsoft.com/azure-stack/operator/azure-stack-find-cloud-id'>Stamp Cloud ID.</a> If you're not sharing diagnostic data or you're running a build earlier than 1910, type N/A.",
            "required": false
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
            "id": "stack_guid",
            "order": 7,
            "controlType": "textbox",
            "displayLabel": "GUID of your Azure Stack environment's Deployment",
            "watermarkText": "Enter the GUID",
            "required": false
        },
        {
            "id": "CA_external",
            "order": 8,
            "controlType": "textbox",
            "displayLabel": "Certificate authority that signed your Azure Stack external certificates",
            "watermarkText": "Enter the name of the Certificate authority",
            "required": false
        },
        {
            "id": "external_CA_expire_day",
            "order": 9,
            "controlType": "textbox",
            "displayLabel": "Next external certificate expiration date",
            "watermarkText": "Enter the date",
            "required": false
        },
        {
            "id": "internal_CA_expire_day",
            "order": 10,
            "controlType": "textbox",
            "displayLabel": "Next internal certificate expiration date",
            "watermarkText": "Enter the date",
            "required": false
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
