# Simple Link & URL Shortener

A zero code URL shortener, using Azure Static Web Apps 😃

Have a Azure Static Web Apps instance, with a custom domain configured. Then simply update `staticwebapp.config.json` with the link names and redirects, then git commit/push your changes.

e.g.

```json
{
  "routes": [
    {
      "route": "/foo",
      "redirect": "https://example.net"
    }
  ]
}
```

## Scripts

To make the experience a little more seamless, two bash scripts are provided

```bash
./link-add <shortname> <url>

./link-remove <shortname>
```

These will update the config file (using `jq`) and push up to GitHub

## Self Hosting - Build your own URL shortener

Clearly you need a domain which is nice and short for this entire endeavour to be worthwhile.

- Clone this repo 
- Remove all the routes from `staticwebapp.config.json` file
- Remove the workflow file from `.github` directory
- Remove the origin remote.
- Push repo to your GitHub account. 
- Then create an Azure Static Webapp pointing at that repo.
- Point your [custom domain at the static web app](https://docs.microsoft.com/en-us/azure/static-web-apps/custom-domain). 