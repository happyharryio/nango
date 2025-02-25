---
sidebar_label: Notion
---

# Notion API wiki

:::note Working with the Notion API?
Please add your learnings, favorite links and gotchas here by [editing this page](https://github.com/nangohq/nango/tree/master/docs/docs/providers/notion.md).

:::

## Using Notion with Nango

Provider template name in Nango: `notion`  
Follow our [quickstart](../quickstart.md) to add an OAuth integration with Notion in 5 minutes.

## App registration & publishing

Register your app [here](https://www.notion.com/my-integrations)  
By default your app is internal only, once you created it you will be able to make it public. There is no review process, unless you want to get listed in the Notion App Gallery.

## Useful links

-   [Notion API docs](https://developers.notion.com/docs/getting-started)
-   [List of available Notion API OAuth scopes](https://developers.notion.com/reference/capabilities) (Notion calls these "capabilities")

## API specific gotchas

-   Notion does not let you pass OAuth scopes (called "capabilities" in the Notion API) with the authorization. Instead you set them when you register your OAuth app (called "integrations" in Notion). When you add a Notion config in Nango, just pass a single whitespace as scopes: `" "`
