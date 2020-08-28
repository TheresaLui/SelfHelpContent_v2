<properties
	pageTitle="Provisioning or deleting Studio (classic) resources"
	description="Provisioning or deleting Studio (classic) resources"
	infoBubbleText="Provisioning or deleting Studio (classic) resources"
	service="microsoft.machinelearningstudioclassic"
	resource="studioclassic"
	authors="likebupt"
	ms.author="keli19"
	articleId="machinelearning-studioclassic-provisioningordeletingstudioclassicresources"
	selfHelpType="generic"
	supportTopicIds="32321856"
	productPesIds="15570"
	cloudEnvironments="public, usnat, ussec"
	ownershipId="AzureML_StudioClassicServices"
/>

# Provisioning or deleting Studio (classic) resources

## **Recommended Steps**

- Notebook feature has been shut down since April, 2020. For free workspaces, there is no way to recover the deleted notebooks; for paid workspaces, the notebook files are still stored in workspace blob storage, under Notebooks container, but it is difficult to recover them because the names are unreadble.
- If a workspace was deleted more than 90 days ago, there is no way to recover it.
- A know issue of cannot delete workspace is that: if you deleted a workspace before August 2020, and create a new workspace with the same name, you cannot find and delete it in azure portal. The new workspace can be used normally but cannot be deleted by user. We have fixed this issue of deletion, but for workspaces created before August 2020, if you intend to delete it, please open a ticket and we will help delete.

## **Recommended Documents**
Microsoft Azure Machine Learning Studio (classic) is a collaborative, drag-and-drop tool you can use to build, test, and deploy predictive analytics solutions on your data. Customers currently using or evaluating Machine Learning Studio (classic) are encouraged to try [Azure Machine Learning designer](https://docs.microsoft.com/azure/machine-learning/concept-designer), which provides drag and drop ML modules plus scalability, version control, and enterprise security.


