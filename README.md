# Zara Scraper API

[![Oxylabs promo code](https://raw.githubusercontent.com/oxylabs/product-integrations/refs/heads/master/Affiliate-Universal-1090x275.png)](https://oxylabs.io/pages/gitoxy?utm_source=877&utm_medium=affiliate&groupid=877&utm_content=zara-scraper-github&transaction_id=102f49063ab94276ae8f116d224b67)


<p align="left">
  <a href="https://dashboard.oxylabs.io"><img src="https://img.shields.io/badge/%F0%9F%9A%80_Get_Started-FF6B35?style=for-the-badge" alt="Get started"></a>
  <a href="https://developers.oxylabs.io/products/web-api"><img src="https://img.shields.io/badge/%F0%9F%93%9A_Documentation-4A90E2?style=for-the-badge" alt="Documentation"></a>
  <a href="https://dashboard.oxylabs.io"><img src="https://img.shields.io/badge/%F0%9F%93%8A_Dashboard-2EA44F?style=for-the-badge" alt="Dashboard"></a>
  <a href="https://discord.gg/Pds3gBmKMH"><img src="https://img.shields.io/badge/%F0%9F%92%AC_Discord-5865F2?style=for-the-badge" alt="Discord"></a>
  <a href="https://www.youtube.com/@oxylabs"><img src="https://img.shields.io/badge/%E2%96%B6%EF%B8%8F_YouTube-FF0000?style=for-the-badge" alt="YouTube"></a>
</p>

Oxylabs [Zara Scraper](https://oxylabs.io/products/scraper-api/ecommerce/zara?utm_source=github&utm_medium=repositories&utm_campaign=product) (part of the Web Scraper API) is a real-time data gathering solution that uses a fast-adapting infrastructure for effortless Zara product data extraction. It combines **automated proxy management, web data access, and parsing** to collect structured data from any public website at scale.. 

This brief guide explains how an Zara Scraper works and provides code examples to get started rigth away.

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
With our Zara Scraper, you can seamlessly gather data exclusive to Zara web pages. Take hold of crucial fashion detail, including clothing prices, user reviews, and garment descriptions, to evaluate the fashion market and stay on top of your competition. For any queries or troubleshooting guidance, feel free to connect with our support team through live chat or drop us an email at support@oxylabs.io.
