---
layout: layouts/pattern.njk
title: Error pages
description: Use error pages to tell users there is an unexpected problem. Explain what has happened and what they can do next.
backlogID: 119
tags:
  - page
---

{% example "error-pages/test-results.njk" %}

## When to use

Use an error page when:

- there is an unexpected technical problem
- users cannot access the service

## When not to use

Do not use this pattern if:

- you can adapt GOV.UK patterns for [page not found](https://design-system.service.gov.uk/patterns/page-not-found-pages/) or [service unavailable](https://design-system.service.gov.uk/patterns/service-unavailable-pages/) 
- a user makes a mistake completing a form – instead, follow the NHS service manual guidance for [error messages](https://service-manual.nhs.uk/design-system/components/error-message) and [errors summaries](https://service-manual.nhs.uk/design-system/components/error-summary)
- a user cannot continue for an expected reason, for example because they are not eligible – instead, check our GitHub discussion on <a href="https://github.com/nhsuk/nhsapp-frontend/issues/411">unhappy path pages</a>

## How to structure an error page

### 1. Main heading

Use the main heading (H1) to explain what is wrong. Start with: "There is a problem" followed by a short description.

If the cause of the error is unknown or complicated, you can use: "There is a technical problem".

### 2. Main body text

You can use the main body text to: 

- give more details 
- set the context for the action that follows 

Keep the text concise. 

### 3. Button

Use a secondary button for an action that may help to resolve the problem. This could include:

- "Try again" (refreshing the page)
- "Log out"

Work closely with developers and the Service Management Team to understand what users can do in the scenario.

Place buttons straight after the body text that sets the context for the action.

{% example "error-pages/referrals.njk" %}

### 4. Secondary body text

If needed, you can use the space beneath the button to:

- let users know about a different way to access the service
- give links to another relevant service

For links to other NHS App services, use a secondary card link.

{% example "error-pages/show-gp-appointments-olc.njk" %}

### 5. Signposting to medical help

Always include signposting to medical help on error pages.

Use the heading: "For urgent medical advice" followed by the text: "Use [111 online](https://111.nhs.uk/) or [call 111](https://111.nhs.uk/)."

### 6. Signposting to technical support

If the Service Management Team agree they can help users in the scenario, use the heading: "For technical help" followed by the text: "Make a note of the error code **xxxxx** and then contact the [NHS App team](https://www.nhs.uk/contact-us/nhs-app-contact-us/)". Insert a relevant error code where the bold text is.

It can help users if they include the error code in the contact form. It helps the Service Management Team to provide them with the relevant help information more quickly.

## If a user is logged out

Logged-out errors do not display the app header or footer.

{% example "error-pages/login.njk" %}

## How not to use

The page should not:

- blame the user
- include breadcrumbs or a back link at the top
- display vague terms or jargon like "500", "504", "bad request" or "we are experiencing technical difficulties"
- use red text to warn people
- use exclamation marks or informal language like "oops"

Avoid giving users too many different links to choose from as a next step. This increases cognitive load, and is problematic for users experiencing high levels of stress or anxiety.

## Research

Research has shown that users may:

- go straight to buttons and links without fully reading error pages
- not notice error codes
- be unsure about whether the problem was their fault or not

We should account for these challenges in our designs and continue to research and iterate the pattern.

### Next steps

We want to learn more about:

- "try again" buttons on errors, and how we can best help users when these fail to solve the problem
- how we can avoid users needing to manually input error codes, for example by pre-populating these codes on our contact form
- how this guidance could evolve into separate pages covering specific errors

## Design history

Find out more about how we arrived at this pattern in our [design history post on error page guidance](https://nhsdigital.github.io/design-history-nhsapp/design-system/2025/06/error-page-guidance/).
