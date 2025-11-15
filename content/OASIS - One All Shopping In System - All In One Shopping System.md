
## Goals
- Intake items of desire
- Scrape Shopping sites for listings 
- Scrape past pricing data on those listings
- Watch price of listing compared to past data
- Decide optimal time to buy
- Notify me when it's time to buy

# Layers
---
#### Shopping site scrapers
###### Amazon
- https://camelcamelcamel.com/
Will scrape CCC directly. Local Ai will be fed info and add to what exists of formatted data. 
###### Aliexpress
- https://www.pricearchive.org/aliexpress.com/item/3256806798479068
Will scrape PriceArchive directly. Notably more data avail than CCC. Local ai can be fed info and add to what exists of formatted data.
#### Auction Site Scrapers
###### Ebay
- https://developer.ebay.com/
###### Shop goodwill
- Ive been told this is simple
Can scrape. Just be normal...
###### FBMP
- Not possible to scrape myself... I don't believe anyone who is


## Web-UI
---
- Will use Flask
##### Pages
- Add items
- Desired items 
- Dashboard of cheap items I may like



## Flow for BIN sites
---
- Server starts
- Add to desire list
- scrape for top listings
- feed unstructured data into ai
- output structured data
- have user check if they like
- start comparing day by day pricing to current price for liked desire items
- when algorithm decided it's time to buy, send an email? text? discord message?
### Flow for Auction sites
---
- server starts
- add to desire list
- scrape for listings
- start in-sync countdown
- feed unstructured data into ai
- output structured data
- user check
- start watching auction prices
- email/text/discord when time is close if price is still good