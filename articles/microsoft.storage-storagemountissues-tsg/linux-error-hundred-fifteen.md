<properties pageTitle="Mount error(115) 'Operation in progress' or 'could not resolve address SA name: Unknown error'"
            description="Mount error(115) 'Operation in progress' or 'could not resolve address SA name: Unknown error'"
            service="Microsoft.Storage"
            resource="Microsoft.Storage/storageAccounts"
            authors="akshaymatmicrosoft"
            ms.author="akshaym"
            displayOrder=""
            selfHelpType="TSG_Content"
            supportTopicIds=""
            resourceTags=""
            productPesIds=""
            cloudEnvironments="public, fairfax, usnat, ussec"
            articleId="4eb87a1e-063c-4fe8-8fc5-805b8e7cab75"
            ownershipId="Centennial_CloudNet_LoadBalancer" />

# Mount error(115) 'Operation in progress' or 'could not resolve address SA name: Unknown error'

This error might be logged when a Linux client is unable to communicate with the Azure Files server, or cannot resolve the address of the Azure Files server

**Resolution**

1. To fix the issue, you have to investigate why the Linux client cannot communicate with Azure Files, or why there is a name resolution issue
2. Here are the steps:
	1. Verify the version of Linux and CIFS Client support SMB 2.1. The client must support at least SMB 2.1 to connect to Azure Files.
    2. Check whether Linux VM in the same datacenter as the Azure Files share. The Linux CIFS client doesn't support encryption yet. So, the VM must be in the same region as the share.
    3. Check the syntax of the mount command the user is using, to make sure it's correct. Here is an example:


        ```bash
        sudo mount -t cifs //.file.core.windows.net/$share-name$ $mount-point$ -o vers=$smb-version$,username=$storage-account-name$,password=$storage-account-key$,dir_mode=0777,file_mode=0777,serverino
        ```

3. Check DNS name resolution. You may receive the following error from the mount command if there are DNS name resolution issues: mount error: could not resolve address for StorageAccountName.file.core.windows.net: Unknown error Any network communication has to start with name resolution. Make sure we can resolve the URL to a valid IP address is a good test to make sure name resolution is working. To verify the DNS name resolution issue, follow the instructions:
4. Ask the user to ping the Files storage URL, and check that it resolves to an Azure IP address. NoteThe IP address that's resolved for .file.core.windows.net will differ from the IP address that's resolved for .blob.core.windows.net, .table.core.windows.net, or .queue.core.windows.net.
5. Use telnet to verify the client can communicate with the server on TCP Port 445 by using the following command: telnet StorageAccountName.file.core.windows.net 445
6. If the port is open, you should see: Connected to file.Storage StampName.store.core.windows.net
7. If the port isn't open, the command will freeze at: Trying IPAddress... Check the IP Tables on the VM to see if the VM is blocking outbound traffic on TCP Port 445 by using the following command: iptables -L If the entry in the IP Table displays as below:

    ```bash
    Chain OUTPUT (policy ACCEPT) 
    target prot opt source destination 
    DROP tcp -- anywhere anywhere tcp dpt:microsoft-ds
    ```

8. In this situation, the TCP Port 445 is blocked, modify the TCP rules to allow outbound traffic on Port 445
9. Check if the user has assigned any Network Security Group to the Virtual Machines for security compliance, which might block traffic to the Azure File Storage services. To fix this issue, create Network Security Group (NSG) rules to allow traffic from Virtual Machine to the Azure Storage (blobs/Files/Tables/Queues) IP address. This should restore connectivity to the storage.

<!--

---
**This is the end of the work flow. Did this TSG resolve your issue?**

1. Yes
2. No

-->