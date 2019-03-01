<properties
	pageTitle="Management/Delete a managed instance"
	description="Management/Delete a managed instance"
	service="microsoft.sql"
	resource="servers"
	authors="rohitnayakmsft"
    ms.author="rohitna"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32608389"
	resourceTags=""
	productPesIds="16259"
	cloudEnvironments="public"
	articleId="c134e400-e1e1-45e2-87e7-ea6773a7eb70"
/>
# Delete a managed instance

## **Recommended Steps**

* Virtual Private Cluster is still present in VNet for 12 hours after last Managed Instance from the subnet has been dropped. This allows instant creation of new instances during that period. At the same time, it blocks dropping of VNet, route and NSG. Please note that existence of any of these resources does not produce any costs. Please wait until Virtual Private Cluster is automatically deleted after 12 hours, then delete remaining resources.
