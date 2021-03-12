<properties
	articleId="issues-creating-nfs-volumes"
	pageTitle="Issues creating or deleting NFS volumes"
	description="Issues creating or deleting NFS volumes"
	authors="b-tonya"
	ms.author="b-tonya"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32740772"
	productPesIds="16469"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureNetAppFiles"
/>
# Issues creating or deleting NFS volumes
---
{
  "$schema": "SelfHelpContent",
  "subscriptionRequired": true,
  "resourceRequired": true,
  "title": "Issues creating or deleting NFS volumes",
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
      "id": "nfs_volume_type",
      "order": 2,
      "controlType": "dropdown",
      "displayLabel": "What is the NFS volume type?",
      "watermarkText": "(i.e. NFSv3, NFSv4.1, NFSv4.1 Kerberos)",
      "dropdownOptions": [
        {
          "value": "NFSv3",
          "text": "NFSv3"
        },
        {
          "value": "NFSv4.1",
          "text": "NFSv4.1 "
        },
        {
          "value": "NFSv4.1 Kerberos",
          "text": "NFSv4.1 Kerberos"
        },
        {
          "value": "dont_know_answer",
          "text": "None of the above"
        }
      ],
      "required": true
    },
    {
      "id": "reverselookup",
      "order": 3,
      "controlType": "dropdown",
      "displayLabel": "Is PTR of AD machine added in DNS?",
      "watermarkText": "Is PTR of AD machine added in DNS?",
      "dropdownOptions": [
        {
          "value": "Yes",
          "text": "Yes"
        },
        {
          "value": "No",
          "text": "No"
        },
        {
          "value": "dont_know_answer",
          "text": "None of the above"
        }
      ],
      "required": false
    },
    {
      "id": "dns_reachable",
      "order": 4,
      "controlType": "dropdown",
      "displayLabel": "Is your DNS server IP addresses reachable?",
      "watermarkText": "If there’s no issues with the DNS server IP addresses, then verify that no firewalls are blocking the access?",
      "dropdownOptions": [
        {
          "value": "Yes",
          "text": "Yes"
        },
        {
          "value": "No",
          "text": "No"
        },
        {
          "value": "dont_know_answer",
          "text": "None of the above"
        }
      ],
      "required": false
    },
    {
      "id": "problem_description",
      "order": 5,
      "controlType": "multilinetextbox",
      "displayLabel": "Provide any additional details",
      "required": true,
      "useAsAdditionalDetails": true
    },
    {
      "id": "error_message",
      "order": 6,
      "controlType": "textbox",
      "displayLabel": "Error message",
      "watermarkText": "What was the error message?",
      "required": false
    }
  ]
}
---
