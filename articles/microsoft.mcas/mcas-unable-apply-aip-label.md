<properties
  pagetitle="I am unable to apply an Azure Information Protection label to a file&#xD;"
  service="microsoft.mcas"
  resource=""
  ms.author="shsagir,nagrand"
  selfhelptype="Generic"
  supporttopicids="32728964"
  resourcetags=""
  productpesids="16031"
  cloudenvironments="public,fairfax,usnat,ussec"
  articleid="mcas-unable-apply-aip-label"
  ownershipid="CloudAppSecurity_API" />
# I am unable to apply an Azure Information Protection label to a file

Most users are able to resolve Azure Information Protection labelling issues using the steps below.

## **Recommended Steps**

To use Azure Information Protection labels in Cloud App Security, make sure that:

1. You have enabled the [Office 365 app connector](https://docs.microsoft.com/cloud-app-security/connect-office-365-to-microsoft-cloud-app-security)
1. The labels are published as part of the policy. If you're using Azure Information Protection labels, the labels must be published through the Azure Information Protection portal. If you migrated to unified labels, the labels must be published through the Office 365 Security and Compliance Center.
1. You have not exceeded the default maximum of applying 100 labels per day. If you want to increase the limit, continue with opening the support ticket.
1. The file is one of the following supported types:
    * Word: docm, docx, dotm, dotx
    * Excel: xlam, xlsm, xlsx, xltx
    * PowerPoint: potm, potx, ppsx, ppsm, pptm, pptx
    * PDF (supported only with unified labeling)
1. The file is not in use (because the file might be locked)
1. The file size is greater than 0 and is less than 50 MB
1. The file does not have any manually applied labels through Azure Information Protection
1. The file does not have any labels applied in SharePoint Online

## **Recommended Documents**

* [Apply labels directly to files](https://docs.microsoft.com/cloud-app-security/azip-integration#apply-labels-directly-to-files)

* [Tutorial: Automatically apply Azure Information Protection classification labels](https://docs.microsoft.com/cloud-app-security/use-case-information-protection)

If you're still experiencing the issue after reviewing the documentation and configurations, continue with opening the ticket.
