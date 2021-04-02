<properties
  pagetitle="V2 - Pipeline Activities - Delete"
  description="V2 - Pipeline Activities - Move and TransformCommon Solutions"
  service=""
  resource=""
  ms.author="chez,zhenqxu"
  selfhelptype="Generic"
  supporttopicids="32680905"
  resourcetags=""
  productpesids="15613"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="7d5dba8e-e49d-11e9-81b4-2a2ae2dbcce4"
  ownershipid="AzureData_DataFactory" />
# V2 - Pipeline Activities - Delete

If you deleted resources by mistake and want to restore:
- For Data Factory resources, go back and choose **Data Factory Administration**
- For other Azure resources, file a ticket to the corresponding services
- For files and folders deleted by Delete Activity, contact support of corresponding data stores

### **Best Practices**

- DO grant sufficient permissions(e.g. list & delete) to folders and files in the data stores
- DO avoid race conditions to delete and write the same files at the same time
- Back up your files before deleting them with the Delete activity, in case you need to restore them in the future
- Turn on [Delete Activity logging](https://docs.microsoft.com/azure/data-factory/delete-activity#syntax) to check logs and know the exact error for files/folders that are failed to be deleted

### **Known Limitations**
- Delete activity that doesn't support deleting a list of folders described by a wildcard
- When using the file attribute filter in delete activity (`modifiedDatetimeStart` and `modifiedDatetimeEnd` to select files to be deleted) make sure to set `wildcardFileName: *` in delete activity, as well.
- Delete activity does not support deleting single files with and asterisk ( * ) or question mark (?) in the file name. You can use wildcard file path to work around this. 

## **Recommended Documents**
[Delete Activity in Azure Data Factory](https://docs.microsoft.com/azure/data-factory/delete-activity)
This article references:
- Supported data stores and file systems
- Examples of using Delete activity
