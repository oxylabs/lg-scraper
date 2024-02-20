# Lg Scraper API

[![Oxylabs promo code](https://user-images.githubusercontent.com/129506779/250792357-8289e25e-9c36-4dc0-a5e2-2706db797bb5.png)](https://oxylabs.go2cloud.org/aff_c?offer_id=7&aff_id=877&url_id=112)

Oxylabs' [Lg Scraper](https://oxylabs.io/products/scraper-api/ecommerce/lg?utm_source=github&utm_medium=repositories&utm_campaign=product) is a data gathering solution allowing you to extract real-time information from an Lg website effortlessly. This brief guide showcases how Lg Scraper works, along with code examples to help you better understand how to use it hassle-free.

### How it works

You can get Lg results by providing your own URLs to our service. We can return the HTML for any page you like.

#### Python code example

The example below illustrates how you can get HTML of Lg page.

```python
import requests
from pprint import pprint

# Structure payload.
payload = {
    'source': 'universal_ecommerce',
    'url': 'https://www.lg.com/us/tvs'
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
Find code examples for other programming languages [**here**](https://github.com/oxylabs/lg-scraper/tree/main/code%20examples)

#### Output Example
```json
{
  "results": [
    {
      "content": "<!DOCTYPE html><html lang=\"en\"><head><meta charSet=\"utf-8\"/><meta name=\"viewport\" content=\"width=dev ... </html>",
      "created_at": "2024-02-20 12:50:31",
      "updated_at": "2024-02-20 12:50:32",
      "page": 1,
      "url": "https://www.lg.com/us/tvs",
      "job_id": "7165689175444823041",
      "status_code": 200
    }
  ]
}
```
With our Lg Scraper, you can smoothly gather public data from any Lg smart TV web page. Accumulate crucial information about different smart TV models, including their prices, ratings, or specifications, to assess market trends and outperform your business rivals. Should you have any inquiries, feel free to reach out to our support team through live chat or send us an email at hello@oxylabs.io.