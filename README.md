# GitHub Oktokit OAuth using Netlify Function

GitHub doesn't support the OAuth Implicit flow so you need some server code to handle Authorization flow so I thought I would use Netlify Functions for it.

Largely based on: [intercom-netlify-oauth](https://github.com/netlify-labs/intercom-netlify-oauth).

## Prior Art

- [gatekeeper](https://github.com/prose/gatekeeper)
- [micro-github](https://github.com/mxstbr/micro-github)

## Setting Up

[Create an OAuth App](https://developer.github.com/apps/building-oauth-apps/creating-an-oauth-app/)

Setup a Netlify project and configure the the following [environment variables](https://docs.netlify.com/configure-builds/environment-variables/); `CLIENT_SECRET` and `REACT_APP_CLIENT_ID`.

[Netlify Dev](https://github.com/netlify/cli/blob/master/docs/netlify-dev.md#netlify-functions).

```
npm install -f netlify-cli
netlify login
netlify link
```

## Running Locally

```
netlify dev
```

Netlify Dev is pretty cool, it can run your server function locally.
