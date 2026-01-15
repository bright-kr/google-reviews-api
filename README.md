# Google Reviews API

[![Promo](https://github.com/bright-kr/LinkedIn-Scraper/blob/main/Proxies%20and%20scrapers%20GitHub%20bonus%20banner.png)](https://brightdata.co.kr/products/serp-api/google-search/reviews)

이 리포지토리는 Google Reviews 데이터를 수집하기 위한 두 가지 접근 방식을 제공합니다:

1. **Free Scraper**: 소규모 프로젝트, 테스트, 개인 연구 및 교육 목적을 위한 가볍고 간단한 솔루션입니다.
2. **Bright Data Google Reviews API**: 엔터프라이즈급의 확장 가능하고 신뢰할 수 있는 고용량 데이터 추출을 위한 견고한 솔루션입니다. [SERP API](https://brightdata.co.kr/products/serp-api)의 일부입니다.

## Table of Contents

- [Free Scraper](#free-scraper)
   - [Setup](#setup)
   - [Quick Start](#quick-start)
   - [Sample Output](#sample-output)
   - [Limitations](#limitations)
- [Bright Data Enterprise Solution](#bright-data-enterprise-solution)
   - [Getting Started](#getting-started)
   - [Direct API Access](#direct-api-access)
   - [Native Proxy-Based Access](#native-proxy-based-access)
- [Advanced Features](#advanced-features)
   - [Feature ID (fid)](#feature-id-fid)
   - [Localization (hl)](#localization-hl)
   - [Sorting and Filtering](#sorting-and-filtering)
   - [Pagination](#pagination)
- [Support & Resources](#support--resources)

## Free Scraper
더 작은 규모로 리뷰를 추출해야 하는 분들을 위한 빠르고 간단한 스크레이핑 도구입니다.

<img width="700" alt="scrape-google-reviews-pizza-place" src="https://github.com/bright-kr/google-reviews-api/blob/main/images/420648584-8f8069c4-3521-49d1-ba77-8eb6e840de2b.png" />

### Setup

**Requirements:**

- Python 3.9 이상
- 브라우저 자동화를 위한 [Playwright](https://playwright.dev/)

**Installation:**

```bash
pip install playwright
playwright install
```

> **Web스크레이핑이 처음이신가요?** 당사의 [Beginner's Guide to Web Scraping with Python](https://brightdata.co.kr/blog/how-tos/web-scraping-with-python)을 확인해 보시기 바랍니다.
> 

### Quick Start

1. [google-reviews-scraper.py](https://github.com/bright-kr/Google-Reviews-API/blob/main/google-reviews-scraper/google-reviews-scraper.py)를 열고 다음 변수를 업데이트합니다:
    - `url` – 비즈니스의 Google Maps URL입니다.
    - `target_reviews` – 스크레이핑할 리뷰 수입니다.
2. 스크립트를 실행합니다.

💡 **Pro Tip:** Google의 안티봇(anti-scraping) 시스템에 의한 탐지를 줄이려면 `HEADLESS = False`로 설정하시기 바랍니다.

### Sample Output

```json
{
    "reviewer_name": "Christopher Huntley (youcancallmemaurice)",
    "reviewer_link": "https://www.google.com/maps/contrib/116348973042381100705/reviews?hl=en-GB",
    "reviewer_image": "https://lh3.googleusercontent.com/a-/ALV-UjXgKzymRM7WTYFkhDuA2_lN5WfE7EYAoBAFPOf2YGxA1e_s72zD9A=w36-h36-p-rp-mo-ba5-br100",
    "rating": 5,
    "date": "a month ago",
    "text": "We took a local tip for the best pizza in Chicago. It's a dive vibe with a very regimented process. The garlic bread was good and the dipping sauce was a nice touch.\n\nPizza came fairly quickly. A standard deep dish with sausage, onion and pepper. Good crust, good flavor for sauce and toppings were perfect.\n\nService was quick and attentive. A great experience.",
    "photos": [
        "https://lh3.googleusercontent.com/geougc-cs/AIHozJIkCwzdm33OdIVsHIJcqdLPauk-Q3Xk0rRjj4SrzOaiMF1L_uQFW4T7jg86meLyB6So7wsJX0Pk6m8NuxUbUF_1OTvutnqJbmwU2olmmiS5Z1A6puOo8oPD6qqBSG0TXO5KyM_B=w300-h450-p",
        "https://lh3.googleusercontent.com/geougc-cs/AIHozJKiYAPlUmW7O1M79DDjuRgbeOJ92t2IqwuUDOXUFOABH6XBoZet4bGsYV_NxK1z2SkaFLktjjaAs1FoI2XMEwjt9uMZKQX2K904RjyymLZ1SA4LKq_a3vttOPJr7bMTJCpEx-Y=w300-h225-p",
        "https://lh3.googleusercontent.com/geougc-cs/AIHozJKvdP93huqqhLlxZZDv3VKpNYVriS8qq8lKoGiFydTTDAgZOtupYcgxfaSu4KPbE4wX16lD4sXMOY10vLRVk8_mrMe2N4Ul9hX1h46-JJ0rCmZcDcXogMr_YlIDIp_ao_S_wxVQgQ=w300-h225-p"
    ],
    "likes_count": "4"
}
```

👉 [전체 JSON 출력](https://github.com/bright-kr/Google-Reviews-API/blob/main/google-reviews-results/reviews_output.json)을 확인해 보시기 바랍니다.


### Limitations

Free Scraper에는 중요한 제약이 있습니다:

- IP 주소 차단 위험이 높습니다
- 리クエスト 볼륨이 제한적입니다
- CAPTCHA가 자주 발생합니다
- 대규모 스크레이핑에는 신뢰성이 떨어집니다

신뢰할 수 있는 대규모 데이터 수집을 위해서는 더 고급 솔루션이 필요합니다.

## Bright Data Enterprise Solution

[Bright Data's Google Reviews API](https://brightdata.co.kr/products/serp-api/google-search/reviews)는 고급 기능과 확장성을 갖춘 구조화된 Google Reviews 데이터를 제공합니다. [SERP API](https://brightdata.co.kr/products/serp-api)와 동일한 고급 기술을 기반으로 하며, 다음을 제공합니다:

- **글로벌 위치 정확도:** 어떤 위치에도 맞게 결과를 조정할 수 있습니다
- **Pay-Per-Success 모델:** 성공한 리クエスト에 대해서만 비용을 지불합니다
- **실시간 데이터:** 최신 리뷰를 수 초 내에 가져올 수 있습니다
- **확장성:** 볼륨 제한 없이 무제한 리クエ스트를 처리합니다
- **비용 효율:** 인프라 및 유지보수 비용을 절감합니다
- **최고 수준의 신뢰성:** 내장된 차단 방지 조치로 일관된 성능을 제공합니다
- **기술 지원:** 필요 시 전문가 지원을 받을 수 있습니다

### Getting Started

1. **Prerequisites:**
    - [Bright Data account](https://brightdata.co.kr/)를 생성합니다(신규 사용자는 $5 크레딧 제공)
    - [API key](https://docs.brightdata.com/general/account/api-token)를 발급받습니다
2. **Setup:** API를 통합하기 위해 [단계별 가이드](https://github.com/bright-kr/Google-Reviews-API/blob/main/setup-serp-api-guide.md)를 따르시기 바랍니다
3. **Implementation Methods:**
    - Direct API Access
    - Native Proxy-Based Access

### Direct API Access

API 엔드포인트로 직접 리クエスト합니다.

**cURL Example:**

```bash
curl https://api.brightdata.com/request \
  -H "Content-Type: application/json" \
  -H "Authorization: Bearer API_TOKEN" \
  -d '{
        "zone": "ZONE_NAME",
        "url": "https://www.google.com/reviews?fid=0x89c259a9b3117469:0xd134e199a405a163&brd_json=1",
        "format": "raw"
      }'
```

**Python Example:**

```python
import requests
import json

url = "https://api.brightdata.com/request"
headers = {"Content-Type": "application/json", "Authorization": "Bearer API_TOKEN"}

payload = {
    "zone": "ZONE_NAME",
    "url": "https://www.google.com/reviews?fid=0x89c259a9b3117469:0xd134e199a405a163&brd_json=1",
    "format": "raw",
}

response = requests.post(url, headers=headers, json=payload)

with open("serp-direct-api.json", "w") as file:
    json.dump(response.json(), file, indent=4)

print("Response saved to 'serp-direct-api.json'.")
```

👉 [전체 JSON 출력](https://github.com/bright-kr/Google-Reviews-API/blob/main/google-reviews-api-results/serp-direct-api.json)을 확인해 보시기 바랍니다.

> **Note:** 파싱된 JSON에는 `brd_json=1`을 사용하고, 파싱된 JSON + 전체 중첩 HTML에는 `brd_json=html`을 사용하시기 바랍니다.
> 

### Native Proxy-Based Access

다음과 같이 프록시 라우팅 방식을 사용할 수도 있습니다:

**cURL Example:**

```bash
curl -i \
  --proxy brd.superproxy.io:33335 \
  --proxy-user "brd-customer-<customer-id>-zone-<zone-name>:<zone-password>" \
  -k \
  "https://www.google.com/reviews?fid=0x89c259a9b3117469:0xd134e199a405a163&brd_json=1"
```

**Python Example:**

```python
import requests
import urllib3

urllib3.disable_warnings(urllib3.exceptions.InsecureRequestWarning)

host = "brd.superproxy.io"
port = 33335
username = "brd-customer-<customer-id>-zone-<zone-name>"
password = "<zone-password>"
proxy_url = f"http://{username}:{password}@{host}:{port}"

proxies = {"http": proxy_url, "https": proxy_url}
url = "https://www.google.com/reviews?fid=0x89c259a9b3117469:0xd134e199a405a163&brd_json=html"
response = requests.get(url, proxies=proxies, verify=False)

with open("serp-native-proxy.json", "w", encoding="utf-8") as file:
    file.write(response.text)

print("Response saved to 'serp-native-proxy.json'.")
```

👉 [전체 JSON 출력](https://github.com/bright-kr/Google-Reviews-API/blob/main/google-reviews-api-results/serp-native-proxy.json)을 확인해 보시기 바랍니다.

> **Note:** 프로덕션 환경에서는 [SSL Certificate Guide](https://docs.brightdata.com/general/account/ssl-certificate)에 설명된 대로 Bright Data의 SSL 인증서를 로드하시기 바랍니다.
>

## Advanced Features
Bright Data의 API는 리뷰 추출을 정밀하게 조정하기 위한 여러 고급 파라メータ를 지원합니다.

### Feature ID (fid)
<img width="700" alt="scrape-google-reviews-building" src="https://github.com/bright-kr/google-reviews-api/blob/main/images/420657506-0bc3b223-adf4-487a-9c75-11679b16907d.png" />

feature ID는 비즈니스 또는 위치에 대한 고유 식별자입니다. 이를 찾는 방법은 다음과 같습니다:

1. 비즈니스 이름으로 Google 검색을 수행합니다
2. 검색 결과 페이지의 소스 코드를 확인합니다(우클릭 후 "View Page Source" 선택)
3. 페이지 내에서 "data-fid"를 검색합니다
4. fid는 다음과 같은 형식으로 표시됩니다: `"fid":"0x89c259a9b3117469:0xd134e199a405a163"`

### Localization (hl)

<img width="700" alt="google-reviews-scraper-building" src="https://github.com/bright-kr/google-reviews-api/blob/main/images/420665500-0f1b630e-cb2a-4125-a7de-64be656a2f5b.png" />

두 글자 언어 코드를 사용하여 선호 언어를 지정합니다.

**Example:**

```bash
curl --proxy brd.superproxy.io:33335 \
     --proxy-user brd-customer-<customer-id>-zone-<zone-name>:<zone-password> \
     "https://www.google.com/reviews?fid=0x89c259a9b3117469:0xd134e199a405a163&hl=fr"
```

이 예시는 프랑스어로 리뷰를 반환합니다.

### Sorting and Filtering

쿼리 파라メータ를 사용하여 리뷰를 정렬하고 필터링할 수 있습니다:

1. **sort**: 리뷰 정렬 방식을 결정합니다.
  
    **Possible values:**
    
    - `sort=qualityScore` (default) - 가장 관련성이 높은 리뷰가 먼저 표시됩니다
    - `sort=newestFirst` - 최신 리뷰가 먼저 표시됩니다
    - `sort=ratingHigh` - 평점이 높은 리뷰가 먼저 표시됩니다
    - `sort=ratingLow` - 평점이 낮은 리뷰가 먼저 표시됩니다
    
    **Example:**
    
    ```bash
    curl --proxy brd.superproxy.io:33335 \
         --proxy-user brd-customer-<customer-id>-zone-<zone-name>:<zone-password> \
         "https://www.google.com/reviews?fid=0x89c259a9b3117469:0xd134e199a405a163&sort=ratingLow"
    ```
    
    이 예시는 평점이 낮은 리뷰를 먼저 반환합니다.

2. **filter**: 특정 키워드를 포함하는 리뷰를 필터링합니다.

    **Example:**
    
    ```bash
    curl --proxy brd.superproxy.io:33335 \
         --proxy-user brd-customer-<customer-id>-zone-<zone-name>:<zone-password> \
         "https://www.google.com/reviews?fid=0x89c259a9b3117469:0xd134e199a405a163&filter=excellent"
    ```
    
    이 예시는 "excellent"라는 단어를 포함하는 리뷰만 반환합니다.

### Pagination

다음 파라メータ로 결과 수를 제어하고 페이지네이션을 관리할 수 있습니다:

1. **start**: 페이지네이션을 관리하기 위해 결과 오프셋을 정의합니다.
    - `start=0` (default) - 첫 번째 결과 페이지
    - `start=10` - 두 번째 결과 페이지
    - `start=20` - 세 번째 결과 페이지
    
    **Example:**
    
    ```bash
    curl --proxy brd.superproxy.io:33335 \
         --proxy-user brd-customer-<customer-id>-zone-<zone-name>:<zone-password> \
         "https://www.google.com/reviews?fid=0x89c259a9b3117469:0xd134e199a405a163&start=10"
    ```
    
    이 예시는 두 번째 페이지의 리뷰를 반환합니다.
    
2. **num**: 페이지당 반환할 결과 수를 정의합니다.
    - `num=10` (default) - 10개의 결과를 반환합니다
    - `num=20` - 20개의 결과를 반환합니다(최대)
    
    **Example:**
    
    ```bash
    curl --proxy brd.superproxy.io:33335 \
         --proxy-user brd-customer-<customer-id>-zone-<zone-name>:<zone-password> \
         "https://www.google.com/reviews?fid=0x89c259a9b3117469:0xd134e199a405a163&num=20"
    ```
    
    이 예시는 한 번의 리クエ스트로 20개의 리뷰를 반환합니다.

## Support & Resources

- **Documentation**: [SERP API Docs](https://docs.brightdata.com/scraping-automation/serp-api/)
- **SEO Use Cases**: [SEO Tracking and Insights](https://brightdata.co.kr/use-cases/serp-tracking)
- **Additional Guides**: [Web Unlocker API](https://github.com/bright-kr/web-unlocker-api), [SERP API](https://github.com/bright-kr/serp-api), [Google Search API](https://github.com/bright-kr/google-search-api), [Google News Scraper](https://github.com/bright-kr/Google-News-Scraper), [Google Trends API](https://github.com/bright-kr/google-trends-api)
- **Technical Articles**:
    - [Best SERP APIs](https://brightdata.co.kr/blog/web-data/best-serp-apis)
    - [Build a RAG Chatbot with SERP API](https://brightdata.co.kr/blog/web-data/build-a-rag-chatbot)
- **Technical Support**: [Contact Us](mailto:support@brightdata.com)