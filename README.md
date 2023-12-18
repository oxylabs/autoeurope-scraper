# Autoeurope Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs’ [Autoeurope Scraper](https://oxylabs.io/products/scraper-api/web/autoeurope?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Autoeurope website effortlessly. This brief guide explains how an Autoeurope Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get Autoeurope results by providing your own URLs to our service. We can return the HTML for any Autoeurope page you like.

#### Python code example

The example below illustrates how you can get HTML of Autoeurope page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://www.autoeurope.eu/car-rental-promotions/'
}

# Get response.
response = requests.request(
    'POST',
    'https://realtime.oxylabs.io/v1/queries',
    auth=('user', 'pass1'),
    json=payload,
)

# Instead of response with job status and results url, this will return the
# JSON response with the result.
pprint(response.json())
```
Find code examples for other programming languages [**here**](https://github.com/oxylabs/autoeurope-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html class=\"ua-opera ua-opera-12 ua-opera-12-14 ua-windows_nt ua-windows_nt-6 ua-win ... </html>",
      "created_at": "2023-12-18 11:17:55",
      "updated_at": "2023-12-18 11:18:22",
      "page": 1,
      "url": "https://www.autoeurope.eu/car-rental-promotions/",
      "job_id": "7142473047071586305",
      "status_code": 200
    }
  ]
}
```
With our Autoeurope Scraper, you can easily extract public data from any Autoeurope web page. Gather necessary vehicle rental information, such as rental rates, customer reviews, or rental descriptions, to evaluate the market and get ahead of your competitors. If you have any queries, reach out to our support team through live chat or email us at hello@oxylabs.io.