---
title: 'Content' 
date: Last Modified
permalink: /getting-started/content/index.htm
toc: true
eleventyNavigation:
  key: Content
  title: Content
  order: 10
---

Good content provides Californians with the information and services they need.

## Our voice

| We are                  | We are not                                              |
| ----------------------- |-------------------------------------------------------- |
| A source of truth       | Expressing opinions                                     |
| Information providers   | Service providers                                       |
| Welcoming to everyone   | Overbearing                                             |
| Friendly                | Fake                                                    |
| Official                | Cold or distant                                         |
| Conversational          | Disrespectful                                           |
| Straightforward         | Blunt                                                   |
| Empathetic              | Apathetic                                               |
| Sensitive toward others | Pretending to save people or know everything about them |

## Our style
We write content that’s user-centered. It’s:
* Clear
* Concise
* Accessible

### Focus on needs and services
Give people what they need and direct them to services. Your website is not about telling people what to think about the government or your agency.

### Requirements, not advice
People come to a government website to find out what they need to do. Do not give advice or make suggestions. Use _should_ as little as possible.

### Plain language
Plain language is clear and accessible to everyone, including readers with disabilities and limited English fluency.

* Use [simple words](https://plainlanguage.gov/guidelines/words/use-simple-words-phrases/) when possible.
  * Do not sacrifice clarity for simplicity.
* Explain jargon when you have to use it.
* Spell out acronyms when first used on a page or in an experience. If you use it later, put the acronym in parentheses after the first use.
  * If an acronym is better known than the full name, use it instead. Do not assume because it's familiar in your workplace that everyone knows it. Default to spelling out the acronym.
* Use positive phrases instead of negative ones. They’re easier to understand.
  * Example: write _lack_ instead of _do not have_.

### Clear sentences
* Use [active voice](https://plainlanguage.gov/guidelines/conversational/use-active-voice/) and strong verbs.
  * Do not use [hidden verbs](https://plainlanguage.gov/guidelines/words/avoid-hidden-verbs/).
* Turn gerunds into verbs where it makes sense.
  * Example: write _help_ instead of _helping_.
* Write in present tense.
* Do not use pronouns like _this_, _those_, and _these_ or references like _as above_. They’re vague. Restate what you’re referring to.
* Write out or abbreviate months in dates. Some cultures interpret 9/5/2020 as May 9, 2020, instead of September 5, 2020.
* Use numerals instead of spelling out numbers.
  * Only go to one decimal place. Only use decimals when you need to.
  * Use commas in numbers over 999. This helps people understand the order of magnitude.

### Reading level
Write at a sixth grade level or lower. Some content may not be able to reach this goal, but look for opportunities to use simpler words and shorter sentences. Check reading levels with the [Hemingway Editor](http://hemingwayapp.com/). Eliminate very hard to read sentences and minimize hard to read sentences.

### Be concise
Use short sentences and paragraphs. They’re easier to read and more accessible for all, regardless of reading level.

* Have one thought per sentence.
* Vary the lengths of your sentences and paragraphs to sound natural.
* Remove words that do not add value.
  * Example: do not say _please_ when telling a reader what to do.
* Be direct and confident.

### Organize content by importance
Put the most important content first on a page. This is often the content that applies to the most people. Content that applies to the least people (like specific groups) last.

### Keep it conversational
Write how you speak. Read your writing out loud to hear how it sounds.

* Imagine each period as a breath and each comma as a pause.
* Use common contractions like _you’ll_, _it’s_, and _we’ll_.
  * Do not use contractions with "not," like _don’t_ and _aren’t_. When skimming, readers see _do_ and _don’t_ as the same.
  * Do not use uncommon contractions like _this’ll_, _y’all_, and _ain’t_.
* Where it makes sense, start sentences with _And_ or _But_ to show the relationship between content and add a smooth transition.
* Refer to people as _you_, and the government or agency as _we_. Don’t use _me_ or _my_. It’s unclear if _me_ refers to the reader or the writer.

We recommend AP Style with one exception: we use the serial comma (also called the Oxford comma) to reduce confusion. It’s the comma that comes before _and_ in: _We brought apples, bananas, and oranges._

### Accessibility
We write for all Californians.

Keep the following people in mind when you write:
* Californians with limited financial resources
* Californians without internet access
* Californians who live in difficult housing situations (like those with domestic violence)
* Californians struggling with depression or suicide
* Californians without a fixed address
* Californians with disabilities
* Communities of color
* Immigrant Californians
* Tribal communities
* Californians with limited or no English fluency
* Rural Californians

When discussing benefits and supports, state:
* Minimum requirements
* Any income restrictions
* If it’s available regardless of immigration status, including:
  * How their personal information is protected
  * Which immigrants are eligible
  * If it counts under the public charge rule

If writing for a specific audience, consider what languages the content should be translated into.

### Get to know the people who use your site
Build Google Analytics and Search Console to find out what people are trying to find on your site and the words they're using to do so. Modify your content or metadata to mirror their language.

Work with user researchers to do deeper testing to understand how well people can complete tasks. You can also discover needs you may not know about.

## Structure and formatting
Well-structured content is easy to read and accessible.

### Headings
Clear headings make pages easier to scan and understand.

* Use sentence case. Capitalize the first word and proper nouns. It’s friendlier and helps readers recognize proper nouns.
* Make the name of your page an h1 header. Only use one h1 header per page.
* Use header levels in ascending numerical order. Do not skip steps. It’s OK to repeat header levels.
* Always have at least one line of text between headers.
* Do not use header tags for full sentences or non-header body text.

Check your heading structure in Google Docs. Select **View** and **Show Document Outline** to confirm they nest appropriately.

### Lead class text
Lead class text makes text larger. Use it to explain the service or topic at the top of the page, underneath the h1. Only use one paragraph (one or two sentences max) of lead class text per page. Use this code to create lead class text:

```
<p class="emphasized">the text you want</p>
```

### Titles
The title appears when you hover over the page tab in a browser. It helps users change between tabs on their browser.

Make the title the page heading followed by a hyphen and the site name. This gives users a full understanding of the page. Here’s an example, including the coding tags: 

```
<title>Content guide - Alpha.CA.gov</title>
```

### Page URLs
Use the h1 of the page to create your URL. This helps search engines find the page.

Replace spaces in the title with hyphens so search engines can read them. Delete the conjunctions, prepositions, and articles as long as the URL still keeps the same meaning.
* A page titled _Hire a licensed contractor for home improvements_ would become _/hire-licensed-contractor-home-improvements_.
* Don’t make _Growing up with diabetes_ into _/growing-diabetes_. This has a different meaning.

Use the site map to build the URL. If the licensed contractor page lives under a page called _Services_, the URL would be: _alpha.ca.gov/services/hire-licensed-contractor-home-improvements_.

Any time the site name is spelled out in content, make it a hyperlink to the homepage.

### Bold, italics, underlining
Make important information or keywords users search for bold. We do not use italics for emphasis.

Do not underline content. Web browsers highlight links automatically. Underlining non-link content confuses readers.

### Links and buttons
Use a button with a form or to highlight something the user wants to do. Links are embedded in text instead of standing alone.

* Link to webpages instead of PDFs as much as possible. Webpages are more accessible across devices, more easily searched, and less likely to break.
* Make the link title match the title of the destination page as much as possible. This helps people know they arrived in the right place.
* When creating a button, be short, descriptive, and distinctive.
* Start with an active verb like **Apply**, **Submit**, or **Search**. This keeps the focus on the user’s needs.
* Do not use _See more_, _Here_, or _View more_. They do not give the user a good idea where they’ll go. These phrases also assume everyone can see.
* Limit number of links so as to make the text more readable. If you have several relevant links, put them in a bulleted list after your main text.
* Have links support comprehension, not disrupt it. Do not link until it's alright to send the user away (after you've conveyed your point).
* Open links in the [the same tab and window](https://www.w3.org/TR/WCAG20-TECHS/G200.html). Only open content in a new tab or window when there's a good reason to do so. Give them [warning](https://www.w3.org/TR/WCAG20-TECHS/G201.html) when a new tab or window will open.

### Notes and disclaimers
When info (especially data in tables or graphs) needs an explanation, follow it with a note to provide clarity. Make the note smaller to signal to the reader that it is secondary info. In WordPress, use this code in the HTML view to create smaller text:

```
<p class="small-text"> … </p>
```

## Content types
Some content is easier to understand in non-paragraph form. Bullet points, alerts, and info boxes also make pages easier to scan. 

### Bullet points
Use bullet points for a list of items that are related. Only use bullet points if there is more than one item in the list.

Put a period at the end of a bullet point if it’s a full sentence.
* _Ask family and friends for contractors they recommend._
* _Search online and read reviews, but consider the source._
* _For repairs, your homeowners insurance might cover the cost and suggest contractors for you._

Do not add a period if the bullet point is not a full sentence. Capitalize the first word of every bullet point.
_Ask the contractor to share the name of their insurance carrier and copies of both their:_
* _Workers’ compensation insurance_
* _General liability insurance_

Be consistent with whether your bullet points are sentences or not.

### Numbered lists
Use numbered lists when a user needs to do tasks in a certain order, like a process. They’re especially helpful if the steps happen across different agencies. 
* Start each task with a verb.
* Provide a high-level summary in the task. Put smaller details in the Show/Hide text.
* Keep the description short, no more than a few paragraphs.
  * If it cannot be condensed, make a guide instead.
* Give each number an [ARIA label](https://www.a11y-101.com/development/aria-label) so screen readers can read them aloud as step one, step two, and so on.
* Link to content that already exists on an agency website. Do not duplicate it. Prepare users with the information they need before they select the link.

An example of a numbered list is [Hire a licensed contractor for home improvements](https://www.alpha.ca.gov/hire-licensed-contractor-home-improvements/).

### Questions and answers
Question and answer format is a great way to address edge cases. Do not use questions and answers to communicate info everyone needs to know.

When creating a question and answer section, just call it _Questions and answers_. Don’t add any information like _Questions and answers about financial help_. If questions and answers cluster around certain topics, use subheaders to organize them.

### Guides
A guide is a comprehensive summary of complex information. It usually spans multiple pages. Side navigation lets users move between pages.

An example of a guide is [Apply for unemployment insurance](https://www.alpha.ca.gov/apply-for-unemployment-insurance/).

### Smart answers
A smart answer gives the user an answer that’s specific to their location or situation. Users enter info into one or two form fields.

* Be clear about any limits of the answer.
  * Example: If we can only look up cities in California, share that up front instead of through an error message. 
* Give the button a descriptive term that anticipates the info the user will receive.
  * Example: **Check your water** instead of **Enter**.
* Make error messages proactive instead of assigning blame.
  * Example: _Enter a city in California_ instead of _You entered a city outside of California_. 

Examples of smart answers are [Find the minimum wage in your city](https://www.alpha.ca.gov/find-minimum-wage-your-city/) and [Check lane closures for your trip](https://www.alpha.ca.gov/check-lane-closures/).

### Guided answers
A guided answer takes users through multiple questions to provide an answer tailored to them.

* When the questions are on separate pages, a **Next** button is helpful. The final button should convey the outcome, like **Check if you qualify**.
* Give users a way to get back to the previous question. Separate it from the buttons used to answer questions. 

An example of a guided answer is [Check if you can get a discounted phone service](https://www.alpha.ca.gov/check-if-you-can-get-discounted-phone-service/).

### Checklists and radio buttons
Use a checklist when you want a user to be able to select multiple options from a list. Use radio buttons if you only want them to select one option.

### Forms
Forms allow users to enter in their information and get an answer specific to them and their needs.

* Create titles for each field. Do not use placeholder text that disappears when the user starts typing. It’s hard to remember what belongs in the field or ensure it’s accurate. Placeholder text also is not accessible.
* Display valid options as a user starts typing to confirm what they can choose.
* Add helper text that appears outside the field if someone makes an invalid entry.
  * Example: _Please enter a nine-digit phone number, like 555-555-5555._
* Include a button to explain what type of results users will get.
  * Example: **Search for your city**.

### Alerts
Alerts highlight important or time-sensitive information like deadlines.
 
### Info boxes
Put important information in an info box to help readers find it quickly while skimming. If the content is urgent, use an alert instead.
 
### Page indexes
A way to give users an outline of a long page is to add a page index at the top.

* Start with a brief sentence that states the most important takeaway on the page.
* Follow with text that introduces the index, like "On this page:"
* Make a bulleted, bolded list of the h2 headers on the page. Do not link subheaders. If something is important enough to appear in the page index, elevate it to an h2 header.
* Make each h2 header an anchor link, and link each item in the index to its corresponding header.
