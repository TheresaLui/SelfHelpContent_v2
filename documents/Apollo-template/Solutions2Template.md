<!--For information about each property, see the Metadata page-->
<properties
	pageTitle="Apollo common solutions"
	description="Apollo common solutions"
	ms.author="bernardm"
	displayOrder=""
	articleId="0008d965-e21e-4e73-80ef-0ccc0765fb0c"
	selfHelpType="Apollo"
        supportTopicIds="7d8fb79f-7fbc-7125-b4dc-3060a75a755d"
        productPesIds="16342,16065,15797,16454,16470"
	cloudEnvironments="public"
	ownershipId="b6015c21-c91a-4248-8d13-426894cd5140"
/>

# Solutions 2.0 template 
<!--Required Title in Level 1 heading for internal reference only--> 

**Directions:** Copy the raw form of this page to create a Solution 2.0 (Apollo) article. <br>
Be sure to review the **Rules** at the end of this template to prevent validation errors and comply with [Authoring guidelines](https://azsupportdocs.azurewebsites.net/elixir/articles/AuthoringGuidelines.html).


## Title - Required

<!--Level 2 Heading required; all other headings use level 3 headings. Clearly and concisely state the specific issue and how the article addresses it. Use sentence capitalization for all headings (capitalize only the first word). 
Example: "Resolve issues related to configuring NetApps by reviewing these best practices." <br>
Alternatively, for how-to or conceptual articles, summarize the article and how the article will help the customer.<br>
For example: "Learn how to adjust resource limits for NetApp files by watching the following video."-->

## Body - Required

<!--The body contains the main content (that is, the solution).  At minimum, it must include meaningful content that clearly addresses the customer's issue.  
- For a solution-based article, include an issue statement and one or more solutions. Prioritize your solutions with the one that's most likely to fix the issue at the top.  
- For a how-to or conceptual article, provide instructions (e.g., steps, video, links, etc.)   
<br> 
Solutions can be comprised of the following components. To format these solutions, go to the next section, ### Solution. 
- Procedures
- Images
- Diagnostics  
- Metrics
- Videos 
- AzureKB and document links
<br>
-->

### Solution
<!--Level heading 3 required. Solutions can include diagnostics, procedures, videos, and inline images. Order your solutions in the body so the most common solutions are at the top. 
- If you have more than one solution, format them into sections, using the following heading:
   :::Section section_name:::
- If you have more than five (5) sections, break your your content into multiple articles.


### Procedures 
<!--Level heading 2 required. Use when the solution is a task-based procedure.-->
For a sequence of tasks, use ordered (numbered) lists.
Example:
1. This is a step
2. This step contains multiple sentences. When a step has multiple complete sentences, use a period to end each sentence.
3. This is a step with a [link](http://)
4. This is a step with inline code: `SELECT name, is_disabled FROM sys.sql_logins`
5. This is a step with multi-line code:

```
[cluster my-cluster]
    FormLayout = selectionpanel
    Category = My Templates
    CategoryOrder = 100
    MaxCount = 200
    Autoscale = $Autoscale
```

For non-sequential tasks, use unordered (bullet) lists.
Example:
* Item1
* Item2
* Item3
	* Sub-ItemA
	* Sub-ItemB

### Images
<!--No heading required. Incorporate images within a solution. Use the following format, replacing "alt text" with a description of what is being shown, without punctuation, to ensure accessibility for all users.-->
![alt text](/images/image.png)

### Diagnostics
<!--Optional. Level 3 heading required. A diagnostic is a capability of Azure Cloud Services that collects data from deployed customer services. Explain how this information can help the customer in defining the issue and how it will determine what action they need to take next.-->

<Insight>  
	<symptomId></symptomId><br>
	<executionText></executionText><br>
	<timeoutText></timeoutText><br>
	<noResultText></noResultText><br>
</Insight>

### Videos
<!--Heading optional. Include a title and caption that describes how the video addresses this issue. Call out highlights of the video and include timecode to save the reader from having to scrub through it. To be accessible, video must include captions, a transcript, and audio description, and is delivered in an accessible media player.-->

### Single video
<!--Description-->

   <video>
	<src></src>	
	<title></title>  
   </video>
   
<!--Steps covered in the video-->


### Multiple video
<!--Description-->

   <videoGroup>
	<video>
	    <src></src>	
	    <title></title> 
	</video>
	<video>
            <src></src>	
	    <title></title> 
	</video>
    </videoGroup>

## More resources 
<!--Optional. Only list links that aren't already listed in the solution. Approved sources include: MS docs, MSDN, and Stack Overflow.
Do not add periods after your document links, even if you introduce the link with a complete sentence.
This is the Apollo schema for AzureKB articles-->


### Additional resources that may help you:
<azureKB>
	<client>Portal</client>
</azureKB>

## Rules
* Provide the minimum requirements for title and body. (See each section for details.)
* Use sentence capitalization for all headings (capitalize only the first word) 
* Use accurate, complete spelling of product, feature, and service names (including capitalization). Don't use an acronym on first mention. 
* Use active, imperative verbs and present tense (not passive verbs; not past or future tense) 
* Use contractions (“don’t” instead of “do not”; “you’ll” instead of “you will”) 
* Use “select,” not “click” 
* Don’t use “please” 
* Only bold UI elements (such as buttons, options) in your procedures. Do not overuse.  
* Use code formatting for code (inline and block), values, parameters, properties, operations, methods, functions, language keywords, and directory and file names 
* Enclose error messages in quotation marks 
* Insert a blank line after every heading
* Don't use more than five (5) sections per article.
* Don't use internal links, which users can't access. This includes `review.microsoft.docs` links and `aka.ms` links.
