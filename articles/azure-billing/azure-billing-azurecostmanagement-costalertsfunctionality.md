<properties
	pageTitle="cost alerts functionality - assistance"
	description="cost alerts functionality"
	service="azure-billing"
	resource="billing"
	authors="prdasneo"
	ms.author="prdasneo"
	displayOrder="1"
	selfHelpType="generic"
	supportTopicIds="32615285"
	resourceTags=""
	productPesIds="15659"
	cloudEnvironments="Public, Blackforest, Fairfax, Mooncake, usnat, ussec"
	articleId="9c58cce1-dcf8-4f7e-a478-a47041597f06"
	ownershipId="ASMS_Billing"
/>

# Assistance with Alerts, budgets or forecasted cost functionality

**Why is the Add budget button disabled for me?**<br>

In order to create a budget, you need one of the following permissions:
* Management Group, Subscription, Resource Group Scopes
* Cost Management Contributor
* Owner
* Contributor
* Enterprise Customer Only: Enrollment, Department, Account Scopes
* Enrollment Admin (set budget at Enrollment scope)
* Department Admin (set budget at Department scope)
* Account Owner (set budget at Account scope)
* Modern Customer Agreement Only: Billing Account, Billing Profile, Invoice Section Scopes
* Azure subscription creator<br>
	
**I created a budget when my cost for the current month was already over-budget. Why did I not receive an alert?**<br>
If you have already exceeded a given cost threshold when you create a budget that alert will not fire. Once a new cycle begins, if you breach the threshold then the alert will fire.<br>

**When should I expect to receive an alert after I exceed one of my defined budget alert thresholds?**<br>
Budgets are evaluated every 4 hours. It takes a minimum of 8 hours for usage data to reach the budgets system. Given this, alerts may take as long as 12 hours to fire after you exceed a threshold.<br>

**Why is the Start date button disabled when I select a Month or Billing month reset period?**<br>
Budgets are aligned to the current calendar month or current billing period (in the case where Billing Month is selected). Therefore, we pre-populate this value for you.<br>

**Why do I not see a graph of my costs in the budget creation experience?**<br>
We need a minimum of 2 months of cost data before we can render a graph to assist you with budget creation.<br>

**Why can't I set a budget against a subscription I just created?**<br>
After the creation of a subscription, the data takes 24-48 hours to process before setting a budget against it.<br>

**Budget API Resources**<br>
REST APIs
* [Budgets API v1](https://docs.microsoft.com/rest/api/consumption/budgets):  Provides operations to create and update budgets. Using the Budgets API, you can set a budget threshold and configure multiple alerts to fire as you approach that threshold. Alerts can trigger an email or an Azure Action Group to perform automation. Note: Filtering for this API does not align with Query API filtering / dimensions.
* [Budgets API v2](https://github.com/Azure/azure-rest-api-specs/blob/master/specification/cost-management/resource-manager/Microsoft.CostManagement/preview/2019-04-01-preview/examples/CreateOrUpdateBudget.json): Create budgets with greater cost filtering capabilities than v1. Filtering aligns to the contract used in our Query and Dimensions APIs. This is the recommended budgets API to use moving forward.
* [Dimensions](https://docs.microsoft.com/rest/api/cost-management/dimensions): Provides operations to get supported dimensions for your usage under a variety of scopes. Using the Dimensions API, you can retrieve a list of dimensions that can be used as inputs for generating queries with the Query API.
* [Query](https://docs.microsoft.com/rest/api/cost-management/query): Provides operations to get aggregated cost and usage data based on the query you supply. Using the Query API, you can specify your desired filtering, sorting and grouping on all available dimensions (which are accessed from the Dimensions API). 

**Forecasted Costs**<br>

**Why don’t I see forecasts for my costs in Cost Analysis?**<br>
There are multiple reasons why the forecast projection might be missing for you in Cost Analysis, some of them are as follows:
1. If your cost data is less than 10 days old, the forecast chart will not load. The model requires at least 10 days of recent cost data for accurate projections<br>
2. If you have selected historic dates, then the forecast chart will not be visible. Please select a date range with future dates for the forecast chart to be displayed<br>
3. If your account has multiple currencies, the forecast chart will only project costs for 'All costs in USD'<br> 

**Why doesn’t the forecast change when I make changes to my resources?**<br>
The forecast model requires a couple of days to account for changes in the account and does not make immediate projections based on change in resources<br>
For larger steps of increase or decrease in resources, the model will take slightly longer to adjust to these changes to account for anomalies<br>

**Why does my forecast increase after I make a reservation or Marketplace purchase?**<br>
The forecast model considers your 'Actual Cost' and does not account for usage and purchase separately.For a one-time purchase, the model will decrease the projections after 10 days to account for the sudden increase in costs<br>

**I want to see forecasts for a single dimension (eg. Meter)**<br>
Forecast currently supports total cost projections and not for individual meters. Hence, when 'Grouped by' a dimension, the projections will be for total of all items in the dimension<br>

## **Recommended Documents**

* [What is Azure Cost Management?](https://docs.microsoft.com/azure/cost-management/overview-cost-mgt)<br>
* [Azure Cost Management best practices](https://docs.microsoft.com/azure/cost-management/cost-mgt-best-practices)<br>
* [Analyze your costs and spending](https://docs.microsoft.com/azure/cost-management/quick-acm-cost-analysis)<br>
* [Explore and analyze costs with Cost analysis](https://docs.microsoft.com/azure/cost-management/quick-acm-cost-analysis)<br>
* [Azure Cost Management: Pricing](https://azure.microsoft.com/services/cost-management/#pricing)<br>
* [Review costs in cost analysis](https://docs.microsoft.com/azure/cost-management-billing/costs/quick-acm-cost-analysis#review-costs-in-cost-analysis)<br>


* [Video tutorial: Create a budget in the Azure portal](https://www.youtube.com/watch?v=ExIVG_Gr45A&t=4s)<br>
* [Prerequisites for viewing and customizing budgets](https://docs.microsoft.com/azure/cost-management-billing/costs/tutorial-acm-create-budgets#prerequisites)<br>
* [Create and manage budgets](https://docs.microsoft.com/azure/cost-management-billing/costs/tutorial-acm-create-budgets#create-a-budget-in-the-azure-portal)<br>
* [Configure automation with Azure Action Groups and Budgets API](https://docs.microsoft.com/azure/cost-management/tutorial-acm-create-budgets#trigger-an-action-group)<br>
* [Use cost alerts to monitor usage and spending](https://docs.microsoft.com/azure/cost-management/cost-mgt-alerts-monitor-usage-spending)<br>
* [Cost Management best practices](https://docs.microsoft.com/azure/cost-management/cost-mgt-best-practices)<br>

**Tutorial videos**
* [Create a budget in the Azure portal](https://www.youtube.com/watch?v=ExIVG_Gr45A&t=4s)<br>
* [Manage costs with the Budgets API and Action Groups](https://www.youtube.com/watch?v=bIhbWyWeNh8&t=3s)<br>
