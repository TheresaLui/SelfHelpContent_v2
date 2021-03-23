<properties
pageTitle="Recover deleted Storage Account Account"
description="Recover deleted Storage Account Apollo Solutions"
ms.author="annayak"
displayOrder=""
articleId="e9b9f540-5337-43b1-9b8f-3a7460f4c2bb"
selfHelpType="Apollo"
resourceRequired="true"
supportTopicIds="5bea99a4-5ba9-8f06-ebb9-00ac608021d2,3ba0cdba-5c03-22bf-e777-7f1cc711153c,fa13d9a7-464b-667e-8eb7-1bd0c450476c,d4ac1605-dd7d-12be-317b-6a7210155d52"
productPesIds="15629,16459,16460,16598,16462,16461"
cloudEnvironments="public"
ownershipId="StorageMediaEdge_XStore"
/>

# Troubleshooting authentication and authorization failures using Apollo

## Recover Deleted Storage Account

### Initiate Account Recovery
Make sure the **right subscription** is selected as the diagnostic runs in the context of the **current subscription** only. 

**Note** : If you intend to recover specific containers, blobs, files, and so on, go back to the **Problem description** tab and select **Recover deleted storage data** as the problem subtype instead. Below diagnostic is for **account recovery** only.<br>
<insight>
  <symptomId>Storage_Account_Recovery_Portal_Insight</symptomId>
  <executionText>We are running a quick check to find recently deleted storage account</executionText>
  <timeoutText>We stopped the check, as it was taking too long</timeoutText>
  <noResultText>No recoverable storage account was found. If you intend to recover specific containers, blobs, files, and so on, go back to the "Basics" tab and select "Recover deleted storage data" as the problem subtype instead.</noResultText>
  <additionalInputsReq>false</additionalInputsReq>
</insight>
