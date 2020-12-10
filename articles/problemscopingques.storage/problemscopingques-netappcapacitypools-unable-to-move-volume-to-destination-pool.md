<properties
	articleId="unable-to-move-volume-to-destination-pool"
	pageTitle="Unable to move volume to destination Pool"
	description="Unable to move volume to destination Pool"
	authors="b-mayada"
	ms.author="b-mayada"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32777917"
	productPesIds="16469"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureNetAppFiles"
/>
# Unable to move volume to destination Pool
---
{
  "subscriptionRequired": true,
  "resourceRequired": true,
  "title": "Unable to move volume to destination capacity pool",
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
      "id": "problem_description",
      "order": 2,
      "controlType": "multilinetextbox",
      "displayLabel": "Provide any additional details",
      "required": true,
      "useAsAdditionalDetails": true
    },
    {
      "id": "source_volume_resource_id",
      "order": 3,
      "controlType": "textbox",
      "displayLabel": "Resource ID of the source volume",
      "watermarkText": "Select the volume and click on properties under Settings to get resource id",
      "required": true
    },
    {
      "id": "source_capacity_pool_service_level",
      "order": 4,
      "controlType": "dropdown",
      "displayLabel": "Service level of the source capacity pool",
      "watermarkText": "QoS type of the source capacity pool",
      "dropdownOptions": [
        {
          "value": "Standard",
          "text": "Standard"
        },
        {
          "value": "Premium",
          "text": "Premium"
        },
        {
          "value": "Ultra",
          "text": "Ultra"
        }
      ]
    },
    {
      "id": "source_capacity_pool_qos",
      "order": 5,
      "controlType": "dropdown",
      "displayLabel": "QoS type of the source capacity pool",
      "watermarkText": "QoS type of the source capacity pool",
      "dropdownOptions": [
        {
          "value": "Auto",
          "text": "Auto"
        },
        {
          "value": "Manual",
          "text": "Manual"
        }
      ]
    },
    {
      "id": "destination_pool_name",
      "order": 6,
      "controlType": "textbox",
      "displayLabel": "Destination capacity pool name",
      "watermarkText": "Destination capacity pool name",
      "required": false
    },
    {
      "id": "destination_pool_service_level",
      "order": 7,
      "controlType": "dropdown",
      "displayLabel": "Service level of the destination pool",
      "watermarkText": "Service level of the destination pool",
      "dropdownOptions": [
        {
          "value": "Standard",
          "text": "Standard"
        },
        {
          "value": "Premium",
          "text": "Premium"
        },
        {
          "value": "Ultra",
          "text": "Ultra"
        }
      ]
    },
    {
      "id": "destination_pool_qos",
      "order": 8,
      "controlType": "dropdown",
      "displayLabel": "QoS type of the destination pool",
      "watermarkText": "QoS type of the destination pool",
      "dropdownOptions": [
        {
          "value": "Auto",
          "text": "Auto"
        },
        {
          "value": "Manual",
          "text": "Manual"
        }
      ]
    }
  ],
  "$schema": "SelfHelpContent"
}
---