# CloudFlare-Workers-Deploy
CLI command to deploy a CF Worker from a GitHub repository

## Instructions

Goto Workers & Pages | Settings

Edit "Build configuration" in the Build section.

In the Deploy field enter

<code>npx wrangler deploy --assets=./ --site-exclude **/.git --compatibility-date YYYY-MM-DD</code>

where

_--assets=_ defines where the files are in the GitHub repository structure (i.e. the root in this example). **DO _NOT_ FORGET THE "=".**<br>
_--site-exclude_ do not included these files in the build (deprecated)<br>
_--compatibility-date_ is date of this build (determines which CF Wrangler code version to run)
