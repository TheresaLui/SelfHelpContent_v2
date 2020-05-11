<properties
    pageTitle="Azure Stack virtual machine"
    description="Azure Stack virtual machine"
    authors="alexsmithMSFT"
    ms.author="alexsmit, mquian, v-miegge"
    selfHelpType="problemScopingQuestions"
    supportTopicIds="32663889,32663907,32663909,32663891,32663893,32663895,32663898,32663915,32663917,32663919,32663911,32663912,32663890,32663908,32663910,32663892,32663894,32663896,32663899,32663914,32663916,32663918,32663920,32663897,32663900,32663901"
    productPesIds="16226"
    ownershipId="StorageMediaEdge_AzureStack_Hub"
    cloudEnvironments="public, Fairfax, usnat, ussec"
    schemaVersion="1"
    articleId="8ccb2fde-3000-4e97-b711-4b07ac45db50"
/>
# Azure Stack virtual machine
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
            "id": "patch_level",
            "order": 2,
            "controlType": "dropdown",
            "displayLabel": "Current Patch Level",
            "watermarkText": "Example: 2002 if your build number is 1.2002.0.35.",
            "dropdownOptions": [
                {
                    "value": "2002",
                    "text": "2002"
                },
                {
                    "value": "1910",
                    "text": "1910"
                },
                {
                    "value": "1908",
                    "text": "1908"
                },
                {
                    "value": "1907",
                    "text": "1907"
                },
                {
                    "value": "Other",
                    "text": "Other"
                }
            ],
            "required": false,
            "infoBalloonText": "Example: Select 1903 if your build number is 1.1903.0.35."
        },
        {
            "id": "build_number",
            "order": 3,
            "controlType": "textbox",
            "displayLabel": "Current Build Number",
            "watermarkText": "Example: 1.1903.0.35",
            "required": false,
            "infoBalloonText": "Includes hotfixes. Learn how to <a href='https://docs.microsoft.com/azure-stack/operator/azure-stack-apply-updates#determine-the-current-version'>determine the current build number</a>"
        },
        {
            "id": "connected_deployment",
            "visibility": "patch_level == 2002",
            "order": 4,
            "controlType": "dropdown",
            "displayLabel": "Can Azure Stack Hub connect to Azure?",
            "watermarkText": "Choose an option",
            "dropdownOptions": [{
                    "value": "Yes",
                    "text": "Yes"
                },{
                    "value": "No",
                    "text": "No"
                },{
                    "value": "dont_know_answer",
                    "text": "Unsure"
                }
            ],
            "required": true
        },
        {
            "id": "cloud_id",
            "visibility": "connected_deployment == Yes",
            "order": 5,
            "controlType": "textbox",
            "displayLabel": "Enter your the Stamp Cloud ID",
            "watermarkText": "Enter the Stamp Cloud ID",
            "infoBalloonText": "Learn how to <a href='https://docs.microsoft.com/azure-stack/operator/azure-stack-find-cloud-id'>find your Stamp Cloud ID</a>",
            "required": true
        },
        {
            "id": "region_name",
            "order": 6,
            "controlType": "textbox",
            "displayLabel": "Region Name",
            "watermarkText": "Name of your Azure Stack region",
            "required": false,
            "infoBalloonText": "If you have more than one Azure Stack environment, Ex: REGION from https://adminportal.REGION.FQDN"
        },
        {
            "id": "tenant_impact",
            "order": 7,
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
            "id": "os_version",
            "order": 8,
            "controlType": "textbox",
            "displayLabel": "What is the OS version of the affected virtual machine?",
            "watermarkText": "Example: Windows Server 2016, Ubuntu 16.04 LTS server kernel 4.10.0-14-generic to 4.10.0-32-generic",
            "required": false
        },
        {
            "id": "tenant_vm_admin",
            "order": 9,
            "controlType": "dropdown",
            "displayLabel": "Is this a tenant or an admin virtual machine?",
            "dropdownOptions": [
                {
                    "value": "Tenant virtual machine",
                    "text": "Tenant virtual machine"
                },
                {
                    "value": "Admin virtual machine",
                    "text": "Admin virtual machine"
                }
            ],
            "required": false
        },
        {
            "id": "how_deploy",
            "order": 10,
            "controlType": "dropdown",
            "displayLabel": "What image was used to deploy the virtual machine?",
            "watermarkText": "Select a option",
            "dropdownOptions": [
                {
                    "value": "Azure Stack image",
                    "text": "Azure stack marketplace image"
                },
                {
                    "value": "custom image",
                    "text": "Custom image"
                }
            ],
            "required": false
        },
        {
            "id": "vm_status",
            "order": 11,
            "controlType": "textbox",
            "displayLabel": "What is the status of the affected virtual machine in the portal?",
            "watermarkText": "",
            "required": false
        },
    {
          "id": "has_worked",
            "order": 12,
            "controlType": "dropdown",
            "displayLabel": "Has this ever worked?",
            "watermarkText": "Choose an option",
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
            "required": false
        },
        {
            "id": "change_before",
            "order": 13,
            "visibility": "has_worked == Yes",
            "controlType": "textbox",
            "displayLabel": "Has anything changed since this issue started?",
           "watermarkText": "Description of what happened before you noticed the issue",
            "required": false
        },
    {
          "id": "perform_steps",
            "order": 14,
            "controlType": "multiselectdropdown",
            "displayLabel": "Select the troubleshooting steps you have completed:",
            "dropdownOptions": [
                {
                    "value": "Restart the virtual machine",
                    "text": "Restart the virtual machine"
                },
                {
                    "value": "Redeploy the virtual machine",
                    "text": "Redeploy the virtual machine"
                },
                {
                    "value": "dont_know_answer",
                    "text": "Other, don't know or not applicable"
                }
            ],
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
