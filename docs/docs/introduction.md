---
slug: '/'
sidebar_label: Introduction
---

# Nango: Get OAuth tokens for APIs. Fast & secure.

## ⭐ Nango at a glance

Nango is a service that contains everything you need to work with APIs that use OAuth.

It contains:

-   a full OAuth dance for 50+ APIs
-   a frontend SDK to trigger new OAuth flows
-   a backend SDK & REST API to retrieve fresh access tokens for your API calls

Nango is easy to try in 5 minutes and can be deployed in 15:

-   1-liner to start a new OAuth flow in your frontend:

```ts
let result = await nango.auth('github', '<user-id>');
```

-   1-liner to retrieve a fresh access token (with our SDK or REST API):

```ts
let token = await nango.getToken('github', '<user-id>');
```

## 📺 1 minute demo {#demo}

Watch us add GitHub OAuth in 1 minute:

<iframe width="864" height="486" src="https://www.youtube.com/embed/S0VJx2KPCQg" title="YouTube video player" frameborder="0" allow="accelerometer; autoplay; clipboard-write; encrypted-media; gyroscope; picture-in-picture; web-share" allowfullscreen></iframe>

## 👾 Out of the box support for 50+ APIs

50+ APIs are preconfigured to work out-of-the-box. Including:

-   **CRM**: Front, Hubspot, Salesforce, etc.
-   **Accounting**: Xero, Sellsy, Zoho Books, etc.
-   **Fintech:** Brex, Stripe, Braintree, Ramp etc.
-   **Developer tools**: GitHub, GitLab, Linear, Jira etc.
-   **Communication**: Gmail, Microsoft Teams, Slack, Discord, Zoom etc.
-   **Productivity**: Asana, Airtable, Google Drive, Google Calendar, Trello, Google sheets, ClickUp etc.
-   **Social**: Twitter, LinkedIn, Reddit, Facebook etc.
-   [and more...](https://nango.dev/oauth-providers)

If your favorite API is missing [open a GitHub issue](https://github.com/NangoHQ/nango/issues/new) or [contribute it right away](https://docs.nango.dev/contribute-api): The API configurations are just simple [entries in a YAML file](https://www.nango.dev/oauth-providers).

## 🛡️ Small, self-contained & ready for production

Nango is purposely small, focused on its one task and easy to deploy in production:

-   Runs as a single docker container
-   Updates easily (`docker pull`)
-   Secured with an API key
-   Managed with a CLI

Nango's community continuously maintains & expands API templates.

## 🔍 Where to learn more

-   Explore [the full list of supported APIs](https://nango.dev/oauth-providers)
-   [Contribute a new provider](contribute-api)
-   Share feedback or ask questions on the [Slack community](https://nango.dev/slack)
-   Check our [blog on native integrations](https://www.nango.dev/blog)

## 🐻 History

Pizzly was originally developed by the team at [Bearer](https://www.bearer.com/?ref=pizzly) with contributions of more than 40+ individuals. Over time the focus of Bearer shifted and they could no longer maintain Pizzly. In late 2022 the team at [Nango](https://www.nango.dev) adopted the project and has since developed it together with the growing Nango community.
