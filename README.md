# Zara Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs’ [Zara Scraper](https://oxylabs.io/products/scraper-api/ecommerce/zara?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Zara website effortlessly. This brief guide explains how an Zara Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get Zara results by providing your own URLs to our service. We can return the HTML for any Zara page you like.

#### Python code example

The example below illustrates how you can get HTML of Zara page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://www.zara.com/ww/en/woman-blazers-l1055.html?v1=2290737'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/zara-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html> <html> <head> <meta charset=\"utf-8\"> <meta name=\"viewport\" content=\"width=device-wid ... </html>",
      "created_at": "2023-12-18 10:37:00",
      "updated_at": "2023-12-18 10:37:02",
      "page": 1,
      "url": "https://www.zara.com/ww/en/woman-blazers-l1055.html?v1=2290737",
      "job_id": "7142462752039115777",
      "status_code": 200
    }
  ]
}
```
With our Zara Scraper, you can seamlessly gather data exclusive to Zara web pages. Take hold of crucial fashion detail, including clothing prices, user reviews, and garment descriptions, to evaluate the fashion market and stay on top of your competition. For any queries or troubleshooting guidance, feel free to connect with our support team through live chat or drop us an email at hello@oxylabs.io.