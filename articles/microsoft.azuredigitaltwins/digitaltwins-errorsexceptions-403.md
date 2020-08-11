<properties
	pageTitle="Forbidden (403)"
	description="Forbidden (403)"
	infoBubbleText="Forbidden (403)"
	service="Azure Digital Twins"
	resource="digitaltwins"
	ms.author="rinisbet"
	displayOrder=""
	articleId="digitaltwins-errorsexceptions-403"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32741634"
	resourceTags=""
	productPesIds="17262"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="AzureDigTwin_DigitalTwins"
/>

# Forbidden (403)

## **Recommended Steps**

Azure Digital twins uses RBAC via integration with Azure Active Directory. As such, to read or write to your models, graph or event routes you need to give the security principal (which may be a user, a group or an application service principal) sufficient roles to access Azure Digital Twins. 

1. Assign the roles through the Azure Portal or execute this command in Azure CLI: `az dt rbac assign-role --dt-name <Azure-Digital-Twins-instance-name> --assignee "<AAD-email>" --role owner`. There may be a delay of up to 10 minutes after executing this command.

## **Recommended Documents**

* Learn more about RBAC in Azure Digital Twins in the "Authorization: RBAC roles for Azure Digital Twins" section of the [security for Azure Digital Twins solutions article](https://docs.microsoft.com/azure/digital-twins/concepts-security#authorization-rbac-roles-for-azure-digital-twins)


