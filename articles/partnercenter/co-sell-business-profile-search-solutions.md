<properties
	pageTitle="Business profile does not appear in Microsoft Solution Provider for certain search queries"
	description="Business profile does not appear in Microsoft Solution Provider for certain search queries"
	infoBubbleText=""
	service="partnercenter"
	resource="csp"
	authors="a-crmire"
	ms.author="a-crmire"
	displayOrder=""
	articleId="partnercenter_cosell_business_profile_Microsoft_solution_provider"
	diagnosticScenario=""
	selfHelpType="generic"
	supportTopicIds="32749459" 
	clientIds='partnercenter'
	resourceTags="csp"
	productPesIds="17004"
	cloudEnvironments="public, fairfax, usnat, ussec"
	ownershipId="PartnerCenter_Cosell"
/>

# Partner Center Business profile does not appear in Microsoft Solution Provider for certain search queries

## **Recommended Steps**

Business profile search results are derived based on filtered profiles which are then ranked. Please check if the filters are applied properly if your profile is appearing only for a certain set of queries

**Criteria for *Best match* category**

Below data from business profiles is used to fetch a filtered list of profiles
1. Location - based on radius
2. Exact match is required with the customer org size and any one of the other field in your business profile
* *Industry expertise*
* *Product*
* *Service type*  
* *Solutions* 
* *Skills and capability*

After fetching the filtered profiles, ranks are assigned to the profiles based on the below earned attributes
* *Azure expert MSP*   
* *Advanced specialization*
* *Endorsements* 
* *Competencies*
* *Past referrals conversion data*

**Criteria for *Most responsive* category**
This section takes in to account, the past performance with respect to the number of referrals received, number of referrals accepted among them, time to accept, number of referrals marked as won etc.

**Criteria for *Nearest to you* category**
This is based on the address that is entered in the search. If a city name is entered in the search, the city center latitude and longitude as determined by bing maps is considered for measuring the distance from the partners location in their profile to the city center

## **Recommended Documents**

* [Understand how search works on the Microsoft Solution Provider page](https://docs.microsoft.com/partner-center/create-a-marketing-profile)
* [Managing business profile](https://docs.microsoft.com/partner-center/create-a-marketing-profile)

