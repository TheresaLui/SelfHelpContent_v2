<properties
	pageTitle="Check if the customer is experiencing open file handle issues"
	description="Check if the customer is experiencing open file handle issues"
	service="microsoft.storage"
	resource="storageAccounts"
	authors="JRMayberry"
	ms.author="rimayber"
	displayOrder=""
	selfHelpType="TSG_Content"
	supportTopicIds=""
	resourceTags=""
	productPesIds=""
	cloudEnvironments="public,fairfax,blackforest,mooncake, usnat, ussec"
	articleId="78b00d6a-7356-4094-9df2-d207ab991dd9"
/>

# How to check if the customer is experiencing open file handle issues

This TSG covers the issues attempting to delete a file/folder in an Azure File Share which has an open handle which prevents deletion. Some common error messages:

1. The specified resource is marked for deletion by an SMB client.
2. rm: cannot remove 'FileName': Device or resource busy
3. rm: cannot remove 'FolderName/FileName': Device or resource busy
4. The action can't be completed because the file is open in another program
5. The process cannot access the file because it is being used by another process.

**Common Causes**
1. An application has an active handle on the file/folder.
2. Customer is unable to delete the files/folder because the files were Created/Opened with **DeleteOnClose** Flag and hence the application took a handle to the file and file will get deleted on its own when the last handle is closed.
    1. The file is to be deleted immediately after all of its handles are closed, which includes the specified handle and any other open or duplicated handles.
    2. If there are existing open handles to a file, the call fails unless they were all opened with the **FILE_SHARE_DELETE** share mode 
    3. Subsequent open requests for the file fail, unless the **FILE_SHARE_DELETE** share mode is specified.

If the customer is experiencing this type of issue, then please proceed. 
