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
- For Data Factory resources, please go back and choose **Data Factory Administration**.
- For other Azure resources, please file ticket to the corresponding services.
- For files and folders deleted by Delete Activity, please contact support of corresponding data stores.
### **Best Practices**

- DO grant sufficient permissions(e.g. list & delete) to folders and files in the data stores.
- DO avoid race conditions to delete and write the same files at the same time.
- May backup your files before deleting them with the Delete activity in case you need to restore them in the future.
- May turn on [Delete Activity logging](https://docs.microsoft.com/azure/data-factory/delete-activity#syntax) to check logs and know the exact error for files/folders that are failed to be deleted.

### **Known Limitations**
- Delete activity does not support deleting list of folders described by wildcard.
- When using file attribute filter in delete activity: modifiedDatetimeStart and modifiedDatetimeEnd to select files to be deleted, make sure to set "wildcardFileName": "*" in delete activity as well.
- Delete activity does not support deleting single file with '*' or '?' in filename. You can use wildcard file path to workaround. 

## **Recommended Documents**
Check out [Delete Activity in Azure Data Factory](https://docs.microsoft.com/azure/data-factory/delete-activity) to learn more about:

- Supported Data Stores and File Systems
- Examples of using Delete Activity. E.g. move files using Copy and Delete Activities, delete specific folders or files, periodically clean up time-partitioned folder or files, clean up files by last modified date.