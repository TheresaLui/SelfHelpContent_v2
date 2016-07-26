<properties
	pageTitle="configuration and management/backup"
	description="configuration and management/backup"
	service="microsoft.web"
	resource="sites"
	authors="aashu"
	displayOrder=""
	selfHelpType="generic"
	supportTopicIds="32542208"
	resourceTags=""
	productPesIds="14748"
	cloudEnvironments="public"
/>

# configuration and management/backup

## **Recommended steps**
Seeing 'Partially Succeeded' when you perform a backup of your Web App? One of the frequent causes for this is that some of your files are in use by application and hence are locked while you performed the backup.You can potentially prevent this by excluding files from the backup process and choosing to backup only what is needed. Please see the article below on how to exclude files from the backup process and choosing to backup only what is needed. Explanation of Back-up Status Code:

1. 0 – InProgress: The backup has been started but has not yet completed.
2. 1 – Failed: The backup was unsuccessful.
3. 2 – Succeeded: The backup completed successfully.
4. 3 – TimedOut: The backup did not finish in time and was cancelled
5. 4 – Created: The backup request is queued but has not been started.
6. 5 – Skipped: The backup did not proceed due to a schedule triggering too many backups.
7. 6 – PartiallySucceeded: The backup succeeded, but some files were not backed up because they could not be read. This usually happens because an exclusive lock was placed on the files.
8. 7 – DeleteInProgress: The backup has been requested to be deleted, but has not yet been deleted.
9. 8 – DeleteFailed: The backup could not be deleted. This might happen because the SAS URL that was used to create the backup has expired.
10. 9 – Deleted: The backup was deleted successfully.

## **Recommended documents**
[Backup a Web App – Requirements, Restrictions and More](https://azure.microsoft.com/documentation/articles/web-sites-backup/)<br>
[How to Restore a Web App](https://azure.microsoft.com/documentation/articles/web-sites-restore/)<br>
[Use REST to back up and restore App Service apps](https://github.com/Azure/azure-content/blob/master/articles/app-service-web/websites-csm-backup.md)<br>
[How to exclude files from the backup process and choosing to backup only what is needed](http://www.zainrizvi.io/2015/06/05/creating-partial-backups-of-your-site-with-azure-web-apps/)
