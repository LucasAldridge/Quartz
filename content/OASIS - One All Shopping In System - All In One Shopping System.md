
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

### Data Management
---
	I'm going to use JSON to manage most info. Desire list will be its own file in JSON format. it'll contain the search term when entered by the user, and other data will be put in place as scrapers run on different listings for the search term. Each listing under the term will have a link, current price, historical pricing as a list of dates and prices, and item count.  
### Algorithm for BIN sites
---
- User inputs search term
- new JSON object created
- scrapers look at search term
- each listing recieves it's own object under the search term's object
- scrapers passively update information on each listing, update JSON
	- historical data doesnt need to get scraped again, just move old current price to historical data section w/ date when new current price is scraped. 
- when every listing for a searchterm has been updated (minimum once every 24 hours) all JSON data fed into ai
- If it's determined to be the optimal time to buy, send ping 

### Algorithm for Auction sites
---
- User inputs search term
- new JSON object created
- scrapers look at search term
-  each listing receives it's own object under the search term's object. 
- countdown for each listing begins
- 15 minutes before end of auction, pinged for auctions still at reasonable price.
- Look into https://github.com/shopgoodwill-auction-sniper/shopgoodwill-sniper
- 