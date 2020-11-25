<properties
  pagetitle="Azure Information Protection client - Unable to apply a classification label&#xD;"
  service="microsoft.aip"
  resource="aip"
  ms.author="orbarak,saseftel"
  selfhelptype="Generic"
  supporttopicids="32727971"
  resourcetags=""
  productpesids="14997"
  cloudenvironments="public,blackforest,mooncake,fairfax,usnat,ussec"
  articleid="protectopencontent_cantapplyclassification"
  ownershipid="AzureIdentity_InformationProtection" />
# Unable to apply a classification label in Azure Information Protection client

## **Recommended Steps**

1. Select **Help and feedback** from the **Protect/Sensitivity** button on the Office ribbon, and then **Reset settings**. 
This action signs out the user, deletes the currently downloaded Azure Information Protection policy, and resets the user settings for the Azure Rights Management service.
2.Sign out all users from Office and try again. Azure Information Protection does not support multiple versions of Office installed or multiple users signed in to Office. See these [requirements](https://docs.microsoft.com/azure/information-protection/requirements#applications). Additionally, Azure Information Protection clients do not support multiple versions of Office on the same computer, or multiple user accounts in Office.
4. If you are still experiencing the issue, collect Azure Information Protection client logs and attach the exported logs to this ticket

### Export Azure Information Protection logs

1. Open an Office document or create a new email in Outlook
2. Select the **Protect** or **Sensitivity** button, and **Help and feedback**
3. Select **Export Logs**
4. Save the logs to your choice of location, and attach them to this service request

## **Recommended Documents**

* [Review Azure Information Protection documentation](https://docs.microsoft.com/azure/information-protection/what-is-information-protection)<br>
* [Review Azure Information Protection subscriptions and features](https://azure.microsoft.com/pricing/details/information-protection)<br>
* [Requirements for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/requirements)<br>
* [Quick start tutorial for Azure Information Protection](https://docs.microsoft.com/azure/information-protection/get-started/infoprotect-quick-start-tutorial)<br>
* [Download Azure Information Protection client](https://www.microsoft.com/download/details.aspx?id=53018)<br>
