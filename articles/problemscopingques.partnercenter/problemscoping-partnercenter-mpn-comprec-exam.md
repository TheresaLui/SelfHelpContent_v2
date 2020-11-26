<properties
       pageTitle="Competency recognition for exams or assessments issues"
       description="Competency recognition for exams or assessments issues ticketing intake form"
       authors="A-COFLOR"
       ms.author="A-COFLOR"
       selfHelpType="problemScopingQuestions"
       supportTopicIds=""
       productPesIds="17007"
       cloudEnvironments="public, fairfax, blackforest, mooncake, ussec, usnat"
       schemaVersion="1"
       articleId="problemscoping_partnercenter_mpn_comprec_exam" 
       clientIds="partnercenter"
	ownershipId="PartnerCenter_MPN_Benefits_and_Competencies"
/>
# Competency recognition for exams or assessments Issues

---
{
   "$schema": "SelfHelpContent",
   "resourceRequired": true,
   "subscriptionRequired": true,
   "title": "Competency recognition for exams or assessments Issues",
   "fileAttachmentHint": "To help us better understand your issue please upload the Partner Center User report, a screenshot provided by the user from "My profile" showing the completed association, the MCP transcript and the Assessment proof",
   "formElements": [
       {
       "id": "learn_more_text",
       "order": 1,
       "controlType": "infoblock",
       "content": "Guidance on where to find or how to obtain the files needed to be uploaded:
The Partner Center User report can be exported by the AccountAdmin or MpnPartnerAdmin from User Management menu.
The MCP transcript (for exams or certifications) passed and not recognized – must be taken from MS Learning and the screenshot for the Assessment proof must be taken from Partner University (useful steps: <a href='https://support.microsoft.com/help/4519831/skills-report-in-partner-center'>Skills report in Partner Center</a>).
Needed steps for the screenshot provided by the user from "My profile" showing the completed association can be find <a href='https://support.microsoft.com/help/2966380/how-to-link-or-unlink-a-mcp-id-to-a-partner-organization'>HERE</a> - section B: Associate Microsoft Learning account (exams and certifications)"
       },
       {
	   "id": "mpn_support_level",
       "order": 2,
	   "controlType": "dropdown",
	   "displayLabel": "What support level are you interested in?",
       "watermarkText":"Please select the support level from the below list",
	   "dropdownOptions": [
	       {
		   "value": "silver_level",
		   "text": "Silver"
	       },
	       {
		   "value": "gold_level",
		   "text": "Gold"
	       },
	       {
		   "value": "dont_know_answer",
		   "text": "Not sure"
	       }
	       ],
	   "required": true
       },
       {
	   "id": "competency_type",
       "order": 3,
	   "controlType": "dropdown",
	   "displayLabel": "What competency are you interested in?",
       "watermarkText":"Please select the Competency from the below list",
	   "dropdownOptions": [
	       {
		   "value": "app_dev",
		   "text": "Application Development"
	       },
	       {
		   "value": "app_integration",
		   "text": "Application Integration"
	       },
	       {
		   "value": "cloud_buss_app",
		   "text": "Cloud Business Application"
	       },
	       {
		   "value": "cloud_crm",
		   "text": " Cloud Customer Relationship Management"
	       },
	       {
		   "value": "cloud_platform",
		   "text": "Cloud Platform"
	       },
	       {
		   "value": "cloud_productivity",
		   "text": "Cloud Productivity"
	       },
	       {
		   "value": "collab_content",
		   "text": "Collaboration and Content"
	       },
	       {
		   "value": "communications",
		   "text": "Communications"
	       },
	       {
		   "value": " data_analytics",
		   "text": "Data Analytics"
	       },
	       {
		   "value": "data_platform",
		   "text": "Data Platform"
	       },
	       {
		   "value": "data-center",
		   "text": "Datacenter"
	       },
	       {
		   "value": "dev_ops",
		   "text": "DevOps"
	       },
	       {
		   "value": "ems_comp",
		   "text": "Enterprise Mobility Management"
	       },
	       {
		   "value": "erp_comp",
		   "text": "Enterprise Resource Planning"
	       },
	       {
		   "value": "messaging_comp",
		   "text": "Messaging"
	       },
	       {
		   "value": "ppm_comp",
		   "text": "Project and Portfolio Management"
	       },
	       {
		   "value": "security_comp",
		   "text": "Security"
	       },
	       {
		   "value": "smb_cloud",
		   "text": "Small and Midmarket Cloud Solutions"
	       },
	       {
		   "value": "windows_devices",
		   "text": "Windows and Devices"
	       },
	       {
		   "value": "dont_know_answer",
		   "text": "Not sure"
	       }
	       ],
	   "required": true
       },
       {
	   "id": "competency_method",
       "order": 4,
	   "controlType": "dropdown",
	   "displayLabel": "What is the option used to attain the competency?",
       "watermarkText":"Please select an option from the below list",
	   "dropdownOptions": [
	       {
		   "value": "app_builder",
		   "text": "Application Builders Option"
	       },
	       {
		   "value": "app_integrator",
		   "text": "Application Integrator Option"
	       },
	       {
		   "value": "azure_consumption",
		   "text": "Azure Consumption Option"
	       },
	       {
		   "value": "big_data",
		   "text": " Big Data Option"
	       },
	       {
		   "value": "cloud_crm_reseller",
		   "text": "Cloud CRM Reseller Option"
	       },
	       {
		   "value": "cloud_engagement",
		   "text": "Customer Engagement Option"
	       },
	       {
		   "value": "data_analytics_beginner",
		   "text": "Data Analytics Beginners Option"
	       },
	       {
		   "value": "data_analytics_specialist",
		   "text": "Data Analytics Specialist Option"
	       },
	       {
		   "value": "data_center",
		   "text": "Datacenter Option"
	       },
	       {
		   "value": "deployment_partner",
		   "text": "Deployment Partner Option"
	       },
	       {
		   "value": "devops_partner",
		   "text": "DevOps Partner Option"
	       },
	       {
		   "value": "distributor",
		   "text": "Distributor Option"
	       },
	       {
		   "value": "enterprise_partner",
		   "text": "Enterprise Partner Option"
	       },
	       {
		   "value": "erp_reseller",
		   "text": "ERP Reseller Option"
	       },
	       {
		   "value": "hosting_opt",
		   "text": "Hosting Option"
	       },
	       {
		   "value": "hybrid_services",
		   "text": "Hybrid Services Partner Option"
	       },
	       {
		   "value": "iot_device_builder",
		   "text": "IoT Device Builder Option"
	       },
	       {
		   "value": "learning_opt",
		   "text": "Learning Option"
	       },
	       {
		   "value": "managed_service",
		   "text": "Managed Service Partner Option"
	       },
	       {
		   "value": "o365_services",
		   "text": "O365 Services Option"
	       },
	       {
		   "value": "oem_partner",
		   "text": "OEM Partner Option"
	       },
	       {
		   "value": "power_bi",
		   "text": "Power BI Option"
	       },
	       {
		   "value": "project_portfolio",
		   "text": "Project and Portfolio Partner Option"
	       },
	       {
		   "value": "service_partner",
		   "text": "Service Partner Option"
	       },
	       {
		   "value": "sharepoint_services",
		   "text": "SharePoint Services Partner Option"
	       },
	       {
		   "value": "smb_partner",
		   "text": "SMB Partner Option"
	       },
	       {
		   "value": "solutions_opt",
		   "text": "Solutions Option"
	       },
	       {
		   "value": "sqlserver_specialist",
		   "text": "SQL Server Specialist Option"
	       },
	       {
		   "value": "surface_hub",
		   "text": "Surface Hub Option"
	       },
	       {
		   "value": "surface_reseller",
		   "text": "Surface Reseller Option"
	       },
	       {
		   "value": "system_builder",
		   "text": "System Builder Option"
	       },
	       {
		   "value": "system_integrator",
		   "text": "Systems Integrator Option"
	       },
	       {
		   "value": "unified_operations",
		   "text": "Unified Operations Option"
	       },
	       {
		   "value": "dont_know_answer",
		   "text": "Not sure"
	       }
	       ],
	   "required": true
       },
       {
	   "id": "problem_description",
	   "order": 5,
	   "controlType": "multilinetextbox",
	   "displayLabel": "Details",
	   "watermarkText": "Please provide any additional information about your issue",
       "infoBalloonText": "If your problem is related to usage or azure consumption, net new customers, revenue or performance recognition (etc), please use the <a href='https://partner.microsoft.com/dashboard/support/mpn/servicerequests/create?stage=2&topicid=76e2d30e-8fa5-c90d-725c-4a999092cfa5'>Competency revenue - performance recognition</a> template. To better understand and learn more about competencies and their requirements before attaining them please use the <a href='https://partner.microsoft.com/dashboard/support/mpn/servicerequests/create?stage=3&topicid=f6d4d9aa-acd2-f7e2-ad7e-1fb5e07f20cf'>Competency requirements</a> template.",
	   "required": true,
	   "useAsAdditionalDetails": true
       },
       {
	   "id": "problem_start_time",
	   "order": 6,
	   "controlType": "datetimepicker",
	   "displayLabel": "Start Date",
	   "watermarkText": "When did your issue begin?",
	   "required": true
       }
   ]
}
---