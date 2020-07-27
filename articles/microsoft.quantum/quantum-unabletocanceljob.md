<properties
	pageTitle="Problems cancelling a job running in a quantum workspace"
	description="When you attempt to cancel a job, it continues to execute."
	infoBubbleText="Job continues to execute despite cancellation"
	service="microsoft.quantum"
	resource="workspaces"
	ms.author="dasto"
	displayOrder=""
	articleId=""
	diagnosticScenario=""
	selfHelpType=""
	supportTopicIds="quantum-unabletocanceljob"
	resourceTags=""
	productPesIds="17040"
	cloudEnvironments="public"
	ownershipId=""
/>

# After cancelling a job it continues to run

You may request to cancel a job after having submitted it, however job cancellations are not guaranteed.

Job cancellations should instead be treated as 'cancellation requests'. Additionally the behavior might differ based on the provider you are using. 

## **Recommended Steps**

1. Please review our provider TODO:[documentation](https://) to establish whether your chosen provider supports cancellation requests
2. If your provider supports cancellation, retry your request as it can take several seconds or even minutes (depending on the provider) for the cancellation request to complete
3. If your issues persists, please record the time of your cancellation requests and raise a support case. A member of the team will help you troubleshoot further. 

## **Recommended Documents**

TODO: Add Documentation Links
* [This is the display text of an external document](https://)

### Notes

* The **Recommended Steps** and **Recommended Documents** headings must be entered as shown above (bolded H2)
* Formatting is not identical to Microsoft Docs - tables do not work, nor [!NOTE] tags
* Your Recommended Steps should be actual steps, not just links to other articles
* Ensure all links to Microsoft docs are non-region-specific, i.e. does not include /en-us/. This does not apply to articles for Mooncake.
* Don't link to internal review documentation - these URLs always start with "review.microsoft.docs", and users are unable to access them
* Do not use aka.ms links
* Copy the raw form of this article to use as a template for your own Common Solution article. Be sure to fill in the metadata!
