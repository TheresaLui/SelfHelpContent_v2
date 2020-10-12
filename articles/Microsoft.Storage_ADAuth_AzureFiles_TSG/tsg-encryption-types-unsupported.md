<properties
    pageTitle="Verify if RC4-HMAC encryption type is enabled on the server"
    description="Verify if RC4-HMAC encryption type is enabled on the server"
    service="microsoft.storage"
    resource="storageAccounts"
    authors="yagohel23"
    ms.author="yagohel"
    displayOrder=""
    selfHelpType="TSG_Content"
    supportTopicIds="32689882"
    resourceTags=""
    productPesIds="1003478"
    cloudEnvironments="public, fairfax, usnat, ussec"
    articleId="21efa5a3-e44b-476c-9861-1d167236a406"
    ownershipID="Centennial_CloudNet_LoadBalancer"
/>

# Verify if RC4-HMAC encryption type is enabled on the server. 

If there is no "**KRB_AP_ERR_MODIFIED**" error in the system event log, it could be possible customer's machine does not have "**RC4-HMAC**" encryption type enabled. 

Azure Files Active Directory authentication only supports the **RC4-HMAC** encryption type.Due to group policy that enforces AES encryption type (or another encryption type), the domain controller may either 1) issue all service tickets to Azure Files identities encrypted as AES or 2) refuse to issue tickets for Azure Files identities due to not supporting the identity's default encryption type.

## How to detect

1. HybridManagement PowerShell module Kerberos Ticket status check
    
    a. Will show unhealthy "Azure Files Health Status" if unsupported encryption type is present in ticket. 

        PS C:\users\ledavies> Get-AzStorageKerberosTicketStatus
        
        Client                     : ledavies @ REDMOND.CORP.MICROSOFT.COM
        Server                     : cifs/kailaniafscustaad.file.core.windows.net @ NTDEV.CORP.MICROSOFT.COM
        KerbTicket Encryption Type : AES-256-CTS-HMAC-SHA1-96
        Ticket Flags               : 0x40a10000 -> forwardable renewable pre_authent name_canonicalize
        Start Time                 : 2/12/2020 13:29:56 (local)
        End Time                   : 2/12/2020 23:29:56 (local)
        Renew Time                 : 2/19/2020 13:28:25 (local)
        Session Key Type           : AES-256-CTS-HMAC-SHA1-96
        Azure Files Health Status  : Unhealthy
        
2. (If module is unavailable to the client), use klist output.

    a. Will show "RSADSI RC4-HMAC(NT)" if the ticket is encrypted with supported encryption type.

       PS C:\users\ledavies> klist
    
       Current LogonId is 0:0x3f29d8
    
       Cached Tickets: (4)
       …
       #3>     Client: ledavies @ REDMOND.CORP.MICROSOFT.COM
            Server: cifs/kailaniafscustaad.file.core.windows.net @ NTDEV.CORP.MICROSOFT.COM
            KerbTicket Encryption Type: AES-256-CTS-HMAC-SHA1-96
            Ticket Flags 0x40a10000 -> forwardable renewable pre_authent name_canonicalize
            Start Time: 2/12/2020 13:29:56 (local)
            End Time:   2/12/2020 23:29:56 (local)
            Renew Time: 2/19/2020 13:28:25 (local)
            Session Key Type: AES-256-CTS-HMAC-SHA1-96
            Cache Flags: 0x200 -> DISABLE-TGT-DELEGATION
        Kdc Called: BR1-NTDEV-DC-60.ntdev.corp.microsoft.com