# BookScraper
Scraping a book store website: https://books.toscrape.com/.

Based on https://realpython.com/web-scraping-with-scrapy-and-mongodb/.

## Dev - Useful commands and information:

### Scrapy
start scraping books:

    scrapy crawl book


### MongoDB
docker image:

    mongodb/mongodb-community-server:8.0.4-ubuntu2204

start image detached, open port and volume persistence:

    export MONGODB_VERSION=8.0.4-ubuntu2204
    docker run --name scraper_db -d -p 27017:27017 mongodb/mongodb-community-server:$MONGODB_VERSION

if restarting the instance:

    docker start

stop image:

    docker stop scraper_db && docker rm scraper_db
