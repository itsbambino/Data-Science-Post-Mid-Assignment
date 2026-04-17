# Data-Science-Post-Mid-Assignment
Web Scraping Assignment
# Project Name: Real-Time Crypto Market Data Scraper

### 1. Project Overview
* **Target Website:** [CoinMarketCap](https://coinmarketcap.com/)
* **Data Fields Extracted:** Rank, Name, Symbol, Price, 1h%, 24h%, 7d%, Market Cap, Volume(24h).
* **Tools Used:** Python, BeautifulSoup4, Selenium, Pandas, WebDriver-Manager.

### 2. Setup Instructions
1. Clone this repo: `git clone [https://github.com/itsbambino/Data-Science-Post-Mid-Assignment]`
2. Install dependencies: `pip install -r requirements.txt`
3. Run script: `DS assignment.ipynb`

### 3. Challenges & Solutions
* **Challenge:** The website uses "Lazy Loading," which only loads the first 14 rows of data in the initial HTML, making it impossible to scrape 100 rows using standard request libraries.
* **Solution:** I integrated **Selenium** to automate a headless Chrome browser. I wrote a script to execute JavaScript commands that scrolled the page down incrementally, triggering the website to load the full list of 100 coins before capturing the page source for parsing.
