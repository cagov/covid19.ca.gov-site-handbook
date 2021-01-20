---
title: Content types
date: Last Modified
permalink: /content/types.html
toc: truePerformance
eleventyNavigation:
  key: Types
  order: 13
  parent: Content
---

Some content is easier to understand in non-paragraph form. Bullet points, alerts, and info boxes also make pages easier to scan. 

## Bullet points
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

Always capitalize the first word of each bullet point.

## Numbered lists
Use numbered lists when a user needs to do tasks in a certain order, like a process. They’re especially helpful if the steps happen across different agencies. 
* Start each task with a verb.
* Provide a high-level summary in the task. Put smaller details in the Show/Hide text.
* Keep the description short, no more than a few paragraphs.
  * If it cannot be condensed, make a guide instead.
* Give each number an [ARIA label](https://www.a11y-101.com/development/aria-label) so screen readers can read them aloud as step one, step two, and so on.
* Link to content that already exists on an agency website. Do not duplicate it. Prepare users with the information they need before they select the link.

An example of a numbered list is [Hire a licensed contractor for home improvements](https://www.alpha.ca.gov/hire-licensed-contractor-home-improvements/).

## Questions and answers
Question and answer format is a great way to address edge cases. Do not use questions and answers to communicate info everyone needs to know.

When creating a question and answer section, just call it _Questions and answers_. Don’t add any information like _Questions and answers about financial help_. If questions and answers cluster around certain topics, use subheaders to organize them.

## Guides
A guide is a comprehensive summary of complex information. It usually spans multiple pages. Side navigation lets users move between pages.

An example of a guide is [Apply for unemployment insurance](https://www.alpha.ca.gov/apply-for-unemployment-insurance/).

## Smart answers
A smart answer gives the user an answer that’s specific to their location or situation. Users enter info into one or two form fields.

* Be clear about any limits of the answer.
  * Example: If we can only look up cities in California, share that up front instead of through an error message. 
* Give the button a descriptive term that anticipates the info the user will receive.
  * Example: **Check your water** instead of **Enter**.
* Make error messages proactive instead of assigning blame.
  * Example: _Enter a city in California_ instead of _You entered a city outside of California_. 

Examples of smart answers are [Find the minimum wage in your city](https://www.alpha.ca.gov/find-minimum-wage-your-city/) and [Check lane closures for your trip](https://www.alpha.ca.gov/check-lane-closures/).

## Guided answers
A guided answer takes users through multiple questions to provide an answer tailored to them.

* When the questions are on separate pages, a **Next** button is helpful. The final button should convey the outcome, like **Check if you qualify**.
* Give users a way to get back to the previous question. Separate it from the buttons used to answer questions. 

An example of a guided answer is [Check if you can get a discounted phone service](https://www.alpha.ca.gov/check-if-you-can-get-discounted-phone-service/).

## Checklists and radio buttons
Use a checklist when you want a user to be able to select multiple options from a list. Use radio buttons if you only want them to select one option.

## Forms
Forms allow users to enter in their information and get an answer specific to them and their needs.

* Create titles for each field. Do not use placeholder text that disappears when the user starts typing. It’s hard to remember what belongs in the field or ensure it’s accurate. Placeholder text also is not accessible.
* Display valid options as a user starts typing to confirm what they can choose.
* Add helper text that appears outside the field if someone makes an invalid entry.
  * Example: _Please enter a nine-digit phone number, like 555-555-5555._
* Include a button to explain what type of results users will get.
  * Example: **Search for your city**.

## Alerts
Alerts highlight important or time-sensitive information like deadlines.
 
## Info boxes
Put important information in an info box to help readers find it quickly while skimming. If the content is urgent, use an alert instead.
 
## Page indexes
A way to help users find information easily on a long page is to add a page index at the top.

* Start with a brief sentence that states the most important takeaway on the page.
* Follow with text that introduces the index, like "On this page you will find:"
* Make a bulleted, bolded list of the h2 headers on the page. Do not link subheaders. If something is important enough to appear in the page index, elevate it to an h2 header.
* Make each h2 header an anchor link, and link each item in the index to its corresponding header.
* Keep the page index to 6 items or less. Fit smaller ideas under larger, umbrella ideas.
