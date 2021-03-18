<properties
    pageTitle="Unable to mount - User is not able to retrieve the Kerberos ticket"
    description="Unable to mount - User is not able to retrieve the Kerberos ticket"
    infoBubbleText="Unable to mount - User is not able to retrieve the Kerberos ticket"
    service="microsoft.storage"
    resource="storageAccounts"
    authors="yagohel23"
    ms.author="yagohel"
    displayOrder=""
    selfHelpType="Diagnostics"
    supportTopicIds="32689882"
    resourceTags=""
    productPesIds="1003478"
    cloudEnvironments="public,fairfax,blackforest,mooncake,usnat,ussec"
    articleId="8409904d-948f-471c-8f46-111280edad4a"
    ownershipID="Centennial_CloudNet_LoadBalancer"
/>

# Unable to mount - User is not able to retrieve the Kerberos ticket
<!--issueDescription-->
For Active Directory Authentication to work properly, we need a valid Kerberos ticket to connect to the storage account. A customer may run into an issue with the `CheckGetKerberosTicket` step if their domain group policy does not have a supported Kerberos encryption type enabled, or if the client has cached credentials for the storage account (in Windows Credential Manager) for the storage account and key.
<!--/issueDescription-->

## **Recommended Steps**

1. Check the error message that the customer sees during the `CheckGetKerberosTicket` step. If the error message is "0x80090303/-2146893053: The specified target is unknown or unreachable", use the following steps:

    * Run the `Cmdkey /list` command from the PowerShell console. This will show a list of all cached credentials on the Windows client.
    * Look for any credentials in the list with the target equal to `<storageaccountname>.file.core.windows.net`. See the following example:
    
    ```
      Target: Domain:target=aaddsrgdiag721.file.core.windows.net
      Type: Domain Password
      User: Azure\AADDsrgdiag721
    ```
    
    * Run the `Cmdkey /delete:<TARGETNAMEFROMLISTABOVE>` to delete cached credentials. See the following example:
    
    ```
            Z:\>cmdkey /delete:Domain:target=aaddsrgdiag721.file.core.windows.net
            CMDKEY: Credential deleted successfully.
    ```
    
    * Re-run the Debug command. If it still fails, proceed to the following tep. 

2. The customer (or their domain administrator) needs to examine their domain group policy for [encryption types allowed for Kerberos](https://docs.microsoft.com/windows/security/threat-protection/security-policy-settings/network-security-configure-encryption-types-allowed-for-kerberos). We currently support RC4-HMAC and AES 256 encryption. AES 128 Kerberos encryption is not yet supported.
3. Make sure that `RC4_HMAC` or `AES_256` are included as a value. If the customer has questions about support for the AES 128 Encryption type, follow the appropriate escalation model to engage with PG. 
4. After we've verified that the customer’s domain policy has the supported Kerberos encryption type enabled, if RC4 HMAC is being used, nothing else needs to be done. 
5. If the AES 256 encryption type is being enforced, there are additional steps to follow in order to enable it at the storage account level: 
    * We introduced AES 256 Kerberos encryption support for Azure Files on-premises AD DS authentication with AzFilesHybrid module v0.2.2.
    * Ask the customer to run the [Update-AzStorageAccountAuthForAES256](https://docs.microsoft.com/azure/storage/files/storage-troubleshoot-windows-file-connection-problems#azure-files-on-premises-ad-ds-authentication-support-for-aes-256-kerberos-encryption) PowerShell command to enable AES 256 support. This command is available only with AzFilesHybrid module v0.2.2.
6. After the appropriate changes are completed, re-run the `Debug-AzStorageAccountAuth` cmdlet to make sure that all the other checks pass successfully. If they do not, go back to the previous step for additional troublehsooting.
7. If the `Debug-AzStorageAccountAuth` cmdlet completes successfully, ask the customer to try mounting the file share. If mount still fails, escalate the issue.
