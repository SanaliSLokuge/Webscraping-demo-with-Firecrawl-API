#  Web Scraping Demo with Firecrawl & BeautifulSoup

This project demonstrates web scraping workflow designed to handle both dynamic and static web content effectively. It mainly uses the Firecrawl API to scrape dynamic, JavaScript-rendered websites that traditional scraping tools cannot fully access. For static pages or as a fallback, it leverages BeautifulSoup with standard HTTP requests to parse HTML content.

The scraper extracts key webpage elements including headlines (h1, h2, h3), paragraphs, links, images, and supports searching for user-specified keywords within paragraph text. If the Firecrawl API is unavailable, returns no usable content, or encounters errors, the program automatically falls back to static scraping to maximize data retrieval reliability.

This dual-approach ensures broad website compatibility and resilient performance, making it practical for real-world web scraping tasks where pages may vary in complexity and rendering methods.

---

##  Features

-  Dynamic JS-rendered scraping via Firecrawl API
-  Static fallback scraping using `requests` + `BeautifulSoup`
-  Keyword search across internal links
-  Element path tracing for search context
-  Headline, image, link, paragraph, and full-text extraction


---

##  Requirements

- Python 3.7+
- 'requests'
- 'beautifulsoup4'

Install with:

```bash
pip install -r requirements.txt
