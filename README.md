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

Colab Notebook link: https://colab.research.google.com/drive/15HR8JrkOPQlQm6LYLpg2rxpAjrQlsfXh?usp=sharing

##  Requirements

- Python 3.7+
- 'requests'
- 'beautifulsoup4'

Install with:

```bash
pip install -r requirements.txt
```

## 🧪 Input/Output Examples

### ✅ Example 1: Extract headlines from a static page
**Input:**
```makefile
URL: https://wiki.openstreetmap.org/  
Choice: 1 (headlines)
```

🔹 Welcome to OpenStreetMap  
🔹 How to Contribute  
🔹 Map Features  
...
```
URL: https://www.bbc.com/  
Choice: 2 (title)
```
Title: BBC - Homepage

```
URL: https://wiki.openstreetmap.org/  
Choice: 3 (text)

```
OpenStreetMap is a map of the world, created by people like you and free to use under an open license. Learn more about the project and how you can contribute...


```
URL: https://wiki.openstreetmap.org/  
Choice: 4 (links)

```
🔗 /wiki/Map_Features  
🔗 /wiki/Editing  
🔗 https://www.openstreetmap.org/about  
...

```
URL: https://wiki.openstreetmap.org/  
Choice: 5 (images)

```
🖼️ /cc-wiki.png  
🖼️ https://upload.wikimedia.org/wikipedia/commons/thumb/1/11/Preferences-system.svg/80px-Preferences-system.svg.png  
🖼️ /w/extensions/OSMCALWikiWidget/resources/osmcal-icon.png  
...
```
URL: https://wiki.openstreetmap.org/  
Choice: 6 (paragraphs)
```
OpenStreetMap is the free and editable map of the world, created by volunteers using local knowledge, GPS tracks and other free sources of information.

Everyone can contribute to OpenStreetMap and use the map data for free, under the Open Database License.

We aim to create and provide free geographic data, such as street maps, to anyone who wants them.
...

```
URL: https://www.bbc.com/  
Choice: 7 (keyword search)  
Keyword: culture

```

🔗 Page: https://www.bbc.com/travel/destinations/middle-east  
  📝 ...helping to preserve traditional Bedouin culture....

🔗 Page: https://www.bbc.com/travel/destinations/europe  
  📝 ...art and culture is transforming a once-neglected stretch...
  📝 ...o its fascinating history and authentic culture....

🔗 Page: https://www.bbc.com/travel/destinations/africa  
  📝 ...rituals and cultures through food....
