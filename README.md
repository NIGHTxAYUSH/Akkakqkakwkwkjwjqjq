# Twitch Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

[![](https://dcbadge.vercel.app/api/server/eWsVUJrnG5)](https://discord.gg/GbxmdGhZjq)

Oxylabs’ [Twitch Scraper](https://oxylabs.io/products/scraper-api/web/twitch?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Twitch website effortlessly. This brief guide explains how an Twitch Scraper works and provides code examples to understand better how you can use it hassle-free.

### How it works

You can get Twitch results by providing your own URLs to our service. We can return the HTML for any Twitch page you like.

#### Python code example

The example below illustrates how you can get HTML of Twitch page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal',
    'url': 'https://www.twitch.tv/directory'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/twitch-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html class=\"tw-root--hover\"><head><meta charset=\"utf-8\"><title>Twitch</title><meta n ... </html>",
      "created_at": "2023-12-18 11:15:54",
      "updated_at": "2023-12-18 11:15:55",
      "page": 1,
      "url": "https://www.twitch.tv/directory",
      "job_id": "7142472540844228609",
      "status_code": 200
    }
  ]
}
```
With our Twitch Scraper, you can efficiently mine public data from any Twitch web page. Gather essential stream data such as viewer count, followers, or channel descriptions, to understand audience behavior and stay on top of the gaming industry trends. If you have any enquiries, our support team is available to assist you through live chat or you can email us at hello@oxylabs.io.
