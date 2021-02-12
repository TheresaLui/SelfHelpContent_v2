# Authoring guidelines

_[JR: In this doc, I have 3 comments re: links. The first two are TBA—after you've
done the TOC—and the last one (in comment) is one I didn't want you to miss. Also see
my question (in comment) re: &quot;acceptable links&quot; (one of the last few bullets here).]
[BV: I revised the intro and added links to two topics (in red).]_

These authoring guidelines will familiarize you with the concepts of the voice, tone, and 
strategy of the Microsoft writing style. We urge you to read these guidelines to further 
your writing skills and and help you comply with company standards for customer-facing 
content.

When you're ready to get started with Apollo, go to **Create an Apollo solution** to
learn about Apollo's unique article requirements. To decide on the Apollo solution 
that will best serve the customer for the issue you're addressing, review **Template and 
examples** , which covers the following solution examples:

- **Issue-based solution**  – Presents a single issue with a single solution, a single issue
with multiple solutions, or multiple issues and solutions. You can state the issues directly,
or, if the solution covers a range of issues, you can show the issues through diagnostics.

- **How-to or conceptual solution**  – Provides step-by-step procedures and/or in-depth
conceptual information, with the purpose of increasing the user&#39;s skill or knowledge for
a specific issue or topic.

At a minimum, the solution must contain substantive content that clearly addresses the issue
or topic. If you don't meet this general minimum—for example, if you include links in the
Resources section and nothing else in the body of the solution—the editors will return the 
solution to you for additional content.

## Writing strategy and style

The purpose of our writing strategy and style is to present a solution with clear, concise 
content in a friendly, dynamic voice that engages the customer, while also meeting Microsoft
style standards. The following tips will help you do this:

**Tone**  – We want our customers to feel that they&#39;ve reached a friendly expert. A conversational, informal tone, rather than a formal tone, helps to convey this. Strategies include addressing the user directly, using positive phrasing as much as possible, and using contractions instead of spelled-out verb phrases.

**Example of a friendly, direct, positive voice**<br>
**Our style:**  You need an ID that looks like this: [someone@example.com]
(mailto:someone@example.com). <br>
**Not our style:**  Do not use an invalid ID.<br>
**Note:**  If, in context, you need to emphasize that the user can't use an invalid ID and no
example is needed, then "Do not use an invalid ID" or "Make sure not to use an invalid ID" is acceptable.

**Example of contractions in verb phrases**<br>
**Our style:** If you don't confirm that you've received the message, you won't be able to proceed.<br>
**Not our style: ** If you do not confirm that you have received the message, you will not be able to proceed.<br>
**Note: ** Focus mainly on -n't contractions, such as "isn't," "don't," "won't," "haven't," and "can't." 
Avoid contracting the verb "is" (The browser's fast, simple, and secure&quot;), which can be harder to read. 
Also avoid double contractions ("You mightn't have..."; instead, spell out "You might not have...").

For more information, see Microsoft brand voice.


**Voice and verbs** – Use an active voice and active verbs rather than a passive voice and passive verbs. 
Active voice and verbs produce more concise sentences. Equally important, they directly engage the customer 
as the active agent ("you," either explicitly or implicitly).

     **Example**<br>
     **Our style: ** You query the service, and the server sends an acknowledgment.<br>
     **Not our style: ** The service is queried, and an acknowledgment is sent.<br>

     **Exceptions:**<br>
     **It's acceptable to use passive voice and verbs in the following cases:**<br>

     **To emphasize an object over an action**<br>
     **Example:**  The file is saved.<br>

     **To de-emphasize the subject or the actor**<br>
     **Example:**  Over 50 conflicts were found in the file.<br>

     **If the customer doesn't need to know who or what is responsible for the action**<br>
     **Example:** The database was purged in January.

**Imperative verbs**  – Use imperative verbs—direct commands to the user—whenever possible, omitting extra 
words. This is the most concise verb form and also directly engages the customer.

      **Example**<br>
      **Our style:**  "Run the following command."<br>
      **Not our style:**  "You can run the following command" OR "The following command is run."


**Verb tense**  – Use present tense, except where past or future tense is necessary. Consistent present tense
is easier to read and less confusing than verb tense that shifts between present, past, and future. Try to 
avoid "will."


     **Example**<br>
     **Our style:** Send a query to the service. The server sends an acknowledgment.<br>
     **Not our style:** If you send a query to the service, the server will send an acknowledgment.<br>
Try to avoid the hypothetical "would" which sounds less definite than present tense.

**Example**<br>
**Our style:** If you send an unsubscribe message, the server removes you from the mailing list.<br>
**Not our style:** If you send an unsubscribe message, the server would then remove you from the 
mailing list.

* **Use sentence capitalization for all headings ** (capitalize only the first word). See [examples]
(https://styleguides.azurewebsites.net/StyleGuide/Read?id=2696&amp;topicid=25357),


* **Use "select," not "click."** "Select" applies across all devices, whereas "click" is specific to mouse action.  
* **Don't use "please."**  You're providing information to a user seeking help, so "please" isn't necessary.
* **Don't use Latin abbreviations or words.** Avoid common Latin abbreviations ("e.g., i.e.,"). 
Instead, spell out "for example" and "that is" Also avoid Latin words such as "via" and "verbatim."
In most instances of "via," you can use "through" instead.

**For more information and additional examples, see **[**Top 10 tips for Microsoft style and voice**](https://styleguides.azurewebsites.net/Styleguide/Read?id=2700) **.**

## Formatting

* **Bold all UI elements**, including buttons, blades, menus, dialogs, windows, fields, or any other feature that has a visible name and involves user action. Don&#39;t use quotation marks or italic font in place of bold font. Be sure to follow the UI label (for example, &quot; **Troubleshoot**&quot;) with its descriptor (for example, &quot;button&quot;).


**Example**
**Our style:** Select the  **Troubleshoot ** button.
**Not our style: ** Select  **Troubleshoot**.

**Example**<br>
**Our style:** In the **Instance** field, specify a value less than 64 characters long.
**Not our style:** In the "Instance" field, specify a value less than 64 characters long.


* **Don't overuse bold in text.** Use bold font occasionally, but excessive bold text can be confusing
to the user, who is trying to quickly figure out the logical hierarchy of the solution. In longer 
solutions or solutions with multiple issues, using bold can be an effective way to make key points
or issues more scannable.

* **Don't use bold for emphasis.**  We generally try to avoid visual emphasis of words, and to build 
emphasis into the structure of the sentence instead. If you need to add visual emphasis, italic font,
not bold.

* **Use code formatting for code (inline and block), values, parameters, properties, operations,
methods, functions, language keywords, and directory and file names.**

     For inline code, use a single backtick (`) at the beginning and end of a code snippet.
     For code samples and other code blocks, use three backticks (```) on the line immediately preceding the code, and on the line immediately following the code.
     Be sure to include a blank line after the last three backticks of a code block.

* **Enclose error messages in text in quotation marks.**

* **Insert a blank line above and below every heading.**  

* **Tables must be created in Markdown.**  Markdown has no syntax specific to tables, but you can use
[extended syntax](https://www.markdownguide.org/extended-syntax/). Also see the 
[Markdown Table Generator](https://www.tablesgenerator.com/markdown\_tables).<br>
**Note:** Be sure to view your table in multiple browser types. A table that looks good in Edge 
might look very different in Chrome, and vice versa.

## Branding

* **Make sure to check correct spelling and capitalization for product, feature, and service names.**
You can find these names in the [Cloud Style Guide A-Z list](https://styleguides.azurewebsites.net/Styleguide/Read?id=2696&amp;topicid=25353) (most Azure names are listed under A, in the left panel).


     **Example**<br>
     **Our style:** the Azure portal<br>
     **Not our style:** Azure Portal


* **At first mention of a product, spell out the full name**, with the acronym or abbreviation in
parentheses. Example: "Azure Active Directory (ADD)." After that, you can use only the acronym ("ADD"). 
In self-help solutions, we don't require "Microsoft" in front of brand names.

* **Capitalize** [**only product and service names**, **not instances**](https://styleguides.azurewebsites.net/StyleGuide/Read?id=2696&amp;topicid=44732). If it&#39;s an instance, lowercase all words.

**Example**<br>
**Our style: ** Use App Service to build web apps, mobile apps, and API apps.<br>
**Not our style: ** Use App Service to build Web Apps, Mobile Apps, and API Apps.

## Accessibility

All non-text content (images, charts, videos) must include alternative text (alt text) to meet [Microsoft Accessibility Standards (MAS)](https://microsoft.sharepoint.com/sites/accessibility/SitePages/Microsoft-Accessibility-Standards-(MAS).aspx) **.**  At a minimum, include an introductory sentence that briefly describes the image, chart, or video.
**Images**  – Provide a brief text description in the link text. Optionally, include a brief text description in an introductory sentence immediately above the image.


**Charts and tables**  – Provide a brief text description in an introductory sentence immediately above
the chart or table.


**Videos**  – Provide a brief text description in the link text, at a minimum. If possible, include 
closed captions in the video, and a link to a video transcript.

For more information, see [detailed accessibility guidance](https://microsoft.sharepoint.com/:w:/s/accessibility/EYMLhyJUw-pPp8B_OmgeFK4BaGeklhNXU8Da7A17ya-v_g?e=U9Fdrx).

Links

* **Use simple, concise phrasing to introduce the link:** "See [link text]" is the best generic phrasing.
In most contexts, it's implicitly clear that the link will contain relevant information. It's acceptable
to use an extended phrase if you need to highlight the purpose of the link.


     **Example of simple, concise phrasing:**<br>
     **Our style:** "See [_link text_]."<br>
     **Not our style:** "If you would like more information, refer to [_link text_]."

     **Examples of extended phrasing:**<br>
     "Learn more about [_link text_]."<br>
     "To create a Site-to-Site VPN gateway connection in Azure portal, see [_link text_]."


* **Under the Resources heading**, if you include a long list of links, you can make the list more
scannable by dividing it into clear categories.


      **Example:**
      "Learn more about creating and managing private endpoints.
       [Link 1]
       [Link 2]
       [Link 3]"

* **Link text must clearly indicate the purpose of link** to help the user decide if they want to 
proceed. ("Here" or "this document" doesn't provide enough information about the link.) 
Descriptive link text also helps to ensure that the content meets Microsoft Accessibility standards.

**Example**<br>
**Our style:**  With Azure Cosmos DB, you can save time managing an on-premises database.<br>
Get started with [videos on the Cosmos DB YouTube channel](https://www.youtube.com/channel/UC9OJ32CzooNJNoP6_iIfxRw/videos).
**Not our style:**  With Azure Cosmos DB, you can save time managing an on-premises database. 
Get started [here].


* **Acceptable links**  are links to Microsoft product documentation and AzureKB.

* **Don't use internal links,**  such as _aka.ms_ links or_ review.microsoft.docs_ links. 
These links aren't accessible to users.   

* **In YouTube links, avoid the ampersand character (&). **This character prevents the video from rendering correctly.
