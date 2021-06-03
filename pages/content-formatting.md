---
title: Formatting content
date: Last Modified
permalink: /content/formatting.html
toc: truePerformance
eleventyNavigation:
  key: Formatting
  order: 12
  parent: Content
---

Well-formatted content is easy to read and accessible.

## Headings
Clear headings make pages easier to scan and understand.

* Use sentence case. Capitalize the first word and proper nouns. It’s friendlier and helps readers recognize proper nouns.
* Make the name of your page an h1 header. Only use one h1 header per page.
  * A good h1 tells people what the page is about and what they’ll find on it. For example, _Apply for unemployment insurance_.
  * Make the h1 concise. For example, _Prepare for a wildfire_ instead of _Steps to prepare for a wildfire_.
* Use header levels in ascending numerical order. Do not skip steps. It’s OK to repeat header levels.
* Exception: Questions in accordion format are always in h4 format, no matter what size header has gone before it.
* Always have at least one line of text between headers.
* Do not use header tags for full sentences or non-header body text.

Check your heading structure in Google Docs. Select **View** and **Show Document Outline** to confirm they nest appropriately.

## Lead class text
Lead class text makes text larger. Use it to explain the service or topic at the top of the page, underneath the h1. Only use one paragraph (one or two sentences max) of lead class text per page. Use this code to create lead class text:

```
<p class="emphasized">the text you want</p>
```

## Titles
The title appears when you hover over the page tab in a browser. It helps users change between tabs on their browser.

Make the title the page heading followed by a hyphen and the site name. This gives users a full understanding of the page. Here’s an example, including the coding tags: 

```
<title>Content guide - Alpha.CA.gov</title>
```

## Page URLs
Use the h1 of the page to create your URL. This helps search engines find the page.

Replace spaces in the title with hyphens so search engines can read them. Delete the conjunctions, prepositions, and articles as long as the URL still keeps the same meaning.
* A page titled _Request a birth certificate_ would become _/request-birth-certificate_.
* Do not make _Prepare for a wildfire_ into _/prepare-wildfire_. This has a different meaning.
* If your URL feels too long, consider shortening the page’s h1. Make sure both give enough detail so people know what the page is about.

Use the site map to build the URL. If the birth certificate page lives under a page called _Services_, the URL would be: _alpha.ca.gov/services/request-birth-certificate_.

Any time a site name is spelled out in content, make it a hyperlink to the homepage.

## Bold, italics, underlining
Make important information or keywords users search for bold. We do not use italics for emphasis.

Do not underline content. Web browsers highlight links automatically. Underlining non-link content confuses readers.

## Links and buttons
Use a button with a form or to highlight something the user wants to do. Links are embedded in text instead of standing alone.

* Link to webpages instead of PDFs as much as possible. Webpages are more accessible across devices, more easily searched, and less likely to break.
  * If you must link to a document, make it a PDF if possible. Word documents, Excel sheets, and PowerPoint presentations require software to view them that people may not have.
  * Indicate if the link is going to a file by providing its extension (like PDF, DOC, or PPT) so people can choose if they want to download it.
* Make the link title match the title of the destination page as much as possible. This helps people know they arrived in the right place.
* When creating a button, be short, descriptive, and distinctive.
* Start with an active verb like **Apply**, **Submit**, or **Search**. This keeps the focus on the user’s needs.
* Do not use _See more_, _Here_, or _View more_. They do not give the user a good idea where they’ll go. These phrases also assume everyone can see.
* Limit number of links so as to make the text more readable. If you have several relevant links, put them in a bulleted list after your main text.
* Have links support comprehension, not disrupt it. Do not link until it's alright to send the user away (after you've conveyed your point).
* Open links in the [the same tab and window](https://www.w3.org/TR/WCAG20-TECHS/G200.html). Only open content in a new tab or window when there's a good reason to do so. Give them [warning](https://www.w3.org/TR/WCAG20-TECHS/G201.html) when a new tab or window will open.

## Notes and disclaimers
When info (especially data in tables or graphs) needs an explanation, follow it with a note to provide clarity. Make the note smaller to signal to the reader that it is secondary info. In WordPress, use this code in the HTML view to create smaller text:

```
<p class="small-text"> … </p>
```
