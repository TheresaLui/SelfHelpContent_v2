<properties
	articleId="unable-to-see-the-volume-after-the-move"
	pageTitle="Unable to see the volume after the move"
	description="Unable to see the volume after the move"
	authors="b-mayada"
	ms.author="b-mayada"
	selfHelpType="problemScopingQuestions"
	supportTopicIds="32777918"
	productPesIds="16469"
	cloudEnvironments="Public,MoonCake,FairFax,BlackForest, usnat, ussec"
	schemaVersion="1"
	ownershipId="AzureNetAppFiles"
/>
# Unable to see the volume after the move
---
{
  "subscriptionRequired": true,
  "resourceRequired": true,
  "title": "Unable to see the volume after the move",
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