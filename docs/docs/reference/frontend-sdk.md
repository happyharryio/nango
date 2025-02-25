---
sidebar_label: Frontend SDK
---

# Nango Frontend SDK

The Nango frontend SDK is [available on NPM](https://www.npmjs.com/package/@nangohq/frontend) with the package `@nangohq/frontend`.

## Instantiating the frontend SDK

Please refer to the [quickstart](/quickstart.md#step-3-trigger-the-oauth-flow-from-the-frontend) for how to instantiate the frontend SDK with your Nango setup.

## Triggering OAuth flows

You trigger OAuth flows with `nango.auth`. This function returns a promise, which resolves if the OAuth flow was successful, and rejects if there was an error.

```js
nango
    .auth('<CONFIG-KEY>', '<CONNECTION-ID>')
    .then((result) => {
        // result is an object with:
        // {
        //      providerConfigKey: '<CONFIG-KEY>',
        //      connectionId: '<CONNECTION-ID>
        // }
    })
    .catch((error) => {
        // Error is an object with:
        // {
        //    error: {
        //      type: 'authorization_cancelled', (or similar)
        //      message: 'Authorization fail: The user has closed the authorization modal before the process was complete.'  (or similar)
        //    }
        // }
    });
```

There is an optional third parameter for this function, but it is currently only used for the special case below.

## Triggering OAuth flows with configurations {#connection-config}

Some API Providers require some connection-specific configuration (e.g. Zendesk, Shopify).

For example, Zendesk has the following authorization URL, where the subdomain is specific to a user's Zendesk account:

```
https://<USER-SUBDOMAIN>.zendesk.com/oauth/authorizations/new
```

To set the subdomain pass in an additional configuration object to `nango.auth()`:

```javascript
nango.auth('zendesk', '<CONNECTION-ID>', { params: { subdomain: '<ZENDESK-SUBDOMAIN>' } });

// Or for Shopify
nango.auth('shopify', '<CONNECTION-ID>', { params: { subdomain: '<SHOPIFY-SUBDOMAIN>' } });
```
