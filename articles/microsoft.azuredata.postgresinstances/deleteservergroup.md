<properties
  pagetitle="Delete Hyperscale Server Group "
  service="microsoft.azuredata"
  resource="postgresinstances"
  ms.author="pookam"
  selfhelptype="Generic"
  supporttopicids="32747901"
  resourcetags=""
  productpesids="17124"
  cloudEnvironments="public, fairfax, usnat, ussec"
  articleid="e1554a02-55d6-4970-9212-49835fef6dbc"
  ownershipid="AzureData_Azure_Arc_enabled_PostgreSQL_Hyperscale" />
# Delete Hyperscale Server Group 

Most users are able to resolve their issues  using the recommended steps below.

## **Recommended Steps**

* [Steps to delete resources from Azure](https://docs.microsoft.com/azure/azure-arc/data/delete-azure-resources)
* You can use the --debug switch to get verbose information about the progress of an instance deletion. Example: azdata arc postgres server delete -n postgres01 --debug
* After completion of a postgres server deletion examine the azdata.log: 

```
tail -f ~/.azdata/logs/azdata.log   #(ctrl+C to stop monitoring)
tail -n 200  ~/.azdata/logs/azdata.log
```

* List the Postgres Instances installed on the system to see if the instance is successfully deleted: `azdata arc postgres server list`
* Deleting a server group does not remove its associated PVCs. This is by design. The intention is to help the user to access the database files in case the deletion of instance was accidental. Deleting PVCs is not mandatory. However it is recommended. If you don't reclaim these PVCs, you'll eventually end up with errors as your Kubernetes cluster will think it's running out of disk space. To reclaim the PVCs, take the following steps:

	* [Reclaim Kubernetes Volumes Persistent Claims](https://docs.microsoft.com/azure/azure-arc/data/delete-postgresql-hyperscale-server-group#reclaim-the-kubernetes-persistent-volume-claims-pvcs) 

Since the only connectivity mode that is offered right now is the indirect mode, deleting an instance from Kubernetes will not remove it from Azure and deleting an instance from Azure will not remove it from Kubernetes. For now, it needs to be a two step process and this will be improved in the future. Going forward, Kubernetes will be the source of truth and Azure will be updated to reflect it on each upload.

* [Delete resources from Azure](https://docs.microsoft.com/azure/azure-arc/data/delete-azure-resources)
* [Steps to Uninstall data controller](https://docs.microsoft.com/azure/azure-arc/data/uninstall-azure-arc-data-controller)

## **Recommended Documents**

- [Steps to Uninstall data controller](https://docs.microsoft.com/azure/azure-arc/data/uninstall-azure-arc-data-controller)
- [Reclaim Kubernetes Volumes Persistent Claims](https://docs.microsoft.com/azure/azure-arc/data/delete-postgresql-hyperscale-server-group#reclaim-the-kubernetes-persistent-volume-claims-pvcs) 
- [Storage Configuration](https://docs.microsoft.com/azure/azure-arc/data/storage-configuration) 
- [Troubleshooting Postgres Hyperscale server groups](https://docs.microsoft.com/azure/azure-arc/data/troubleshoot-postgresql-hyperscale-server-group)