<properties 
    pageTitle="I should have received an E-mail for an alert that fired"
    description="General troubleshooting guide for missing e-mail from alerts."
    infoBubbleText="Some suggestions have been found to help solve your missing e-mail issue quicker."
    service="microsoft.insights"
    resource="components"
    authors="debugthings"
    articleId="insights_missingemail"
    displayOrder="5"
    selfHelpType="resource"
    cloudEnvironments="public"
    productPesIds="15693" 
    supportTopicIds="32546625"
 />
# I should have received an E-mail for an alert that fired
## **Recommended steps**
If you're certain that an alert has generated an event but has not sent an e-mail notification you should check the following:

1. The e-mail client SPAM settings (Outlook, Gmail)
2. The e-mail server SPAM/quarantine settings (Exchange, O365, G Suite)
3. Any e-mail security appliances (Barracuda, Cisco)
4. If the e-mail is a distribution list, make sure it can receive external e-mails
5. Look for any unsubscribe e-mail notifications
  * If this goes to a distribution list ask your colleagues with access to check as well

## **Recommended documents**
### E-Mail Client
[Outlook SPAM Settings](https://support.office.com/article/overview-of-the-junk-email-filter-5ae3ea8e-cf41-4fa0-b02a-3b96e21de089)<br>
[Gmail SPAM Settings](https://support.google.com/mail/answer/6579?hl=en)<br>
### E-Mail Server
[O365 Safe Sender](https://docs.microsoft.com/office365/SecurityCompliance/create-organization-wide-safe-sender-or-blocked-sender-lists-in-office-365)<br>
[Exchange SPAM Quarantine](https://docs.microsoft.com/Exchange/antispam-and-antimalware/antispam-protection/spam-quarantine)<br>
[Exchange Sender Filtering](https://docs.microsoft.com/Exchange/antispam-and-antimalware/antispam-protection/sender-filtering)<br>
[G Suite Approved Sender Settings](https://support.google.com/a/answer/2368132)<br>
### Distribution List
[Exchange Delivery Restrictions](https://docs.microsoft.com/Exchange/recipients/user-mailboxes/message-delivery-restrictions#use-the-eac-to-place-message-delivery-restrictions)<br>
[G Suite Groups External Members](https://support.google.com/a/answer/167097)<br>
### Security Appliance
[Barracuda Whitelist Settings](https://campus.barracuda.com/product/websecurityservice/doc/6553671/whitelist-and-blacklist-rules/)<br>
[Cisco Whitelist Settings](https://www.cisco.com/c/en/us/support/docs/security/email-security-appliance/118585-qa-esa-00.html)<br>

