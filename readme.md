# Simple Link & URL Shortener

A zero code URL shortener, using Azure Static Web Apps 😃

Simply update `staticwebapp.config.json` with the link names and redirects, then git commit/push

e.g.

```json
  "routes": [
    {
      "route": "/foo",
      "redirect": "https://example.net"
    }
  ]
```

Point your [custom domain at the static web app](https://docs.microsoft.com/en-us/azure/static-web-apps/custom-domain)

Done 🤪