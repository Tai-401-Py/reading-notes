# Web Scraping

---

## What is web scraping

Web scraping is the technique to automatically access and extract large amounts of data from a website. 

Note: When scraping a site, run through terms and conditions, most sites forbid commercial use. 

Start by inspecting the site and finding the route to the data you want to scrape.

Remember to include a `time.sleep(1)` to prevent most sites from flagging us as spammers.

## Techniques

Human Copy-Paste - Simplest form, manually copy and pasting of data.

Text pattern matching - Using regex or grep to locate data. 

HTTP Programming - Static and Dynamic can be retrieved by using socket programming

HTML Parsing - Many websites have large collection of pages generated dynamically from an underlying structured database. Similar data is typically encoded into similar pages. When data mining, a program will detect the templates

Dom Parsing - By embedding a browser you can use languages like Xpath to parse the DOM tree. 

Computer Vision - There are current efforts to use machine learning to scrape data. 

### How to scrape without being blocked

1. DONT BE A NOZZLE ABOUT IT! 
2. Respect the robots.txt - If you insist on still scraping remember these
3. Don't scrape too fast - Slow your crawler to treat the wesite nicely. By putting random sleep calls in between pages. Try between 10-20 sec per call. 
4. Don't follow the same pattern - incorperate random clicks and mouse movement on page to mimic human movement. 
5. Don't make too many requests from the same IP in a short amount of time - Rotate through proxies. 
6. Remember you proper headers to pretend to be a browser USER-AGENT

Beware of honeypot traps - When follwoing links make sure they have proper visibility. Some honeypot links to detect spiders will have CSS style display:none

Don't Scrape from behind a login, this can lead to you being banned.

PYTHON TESSERACT CAN BYPASS CAPTCHAS! 



