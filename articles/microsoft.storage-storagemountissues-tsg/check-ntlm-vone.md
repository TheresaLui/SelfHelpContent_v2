<properties pageTitle="Check NTLMv1"
            description="Check NTLMv1"
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
            articleId="1509511e-d720-4425-a75c-feaa9157822f"
            ownershipId="Centennial_CloudNet_LoadBalancer" />

# Check NTLMv1
**How to check NTLMv1**

1. System error 53 or system error 87 can occur if NTLMv1 communication is enabled on the client
2. Azure Files supports only NTLMv2 authentication
3. Having NTLMv1 enabled creates a less-secure client
4. Therefore, communication is blocked for Azure Files
5. To determine whether this is the cause of the error, verify that the following registry subkey is set to a value of 3:

    **HKLM | SYSTEM | CurrentControlSet | Control | Lsa > LmCompatibilityLevel**

<!---

---
**This is the end of the work flow. Did this TSG resolve your issue?**

1. Yes
2. No

-->