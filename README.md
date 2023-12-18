# Weibo Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs’ [Weibo Scraper](https://oxylabs.io/products/scraper-api/web/weibo?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Weibo website effortlessly. This brief guide explains how an Weibo Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get Weibo results by providing your own URLs to our service. We can return the HTML for any Weibo page you like.

#### Python code example

The example below illustrates how you can get HTML of Weibo page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://us.weibo.com/index'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/weibo-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "\ufeff<!doctype html>\r\n<html prefix=\"og: http://ogp.me/ns#\">\r\n<head>\r\n<meta charset=\"utf-8\">\r\n<meta name= ... </html>",
      "created_at": "2023-12-18 11:16:23",
      "updated_at": "2023-12-18 11:16:26",
      "page": 1,
      "url": "https://us.weibo.com/index",
      "job_id": "7142472662256727041",
      "status_code": 200
    }
  ]
}
```
With our Weibo Scraper, you can easily extract public data from any Weibo web page. Gather essential information such as user demographics, trending topics, or popular hashtags to understand the market trends and stay ahead of your competition. If you encounter any issues or have any inquiries, feel free to reach our support team through live chat or email us at hello@oxylabs.io.