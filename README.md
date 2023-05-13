## Amazon Review Scraper
download a CSV of up to 5,000 reviews for any Amazon product.

#### installation
first [install Ruby](https://install.founderhacker.com/steps/choose_os). then ensure the following Ruby gems are installed (`gem install <gem_name>`):

* `watir`
* `headless`

next (optional), move the `amz_reviews` file (from this repo) to an executable path. for Mac users this is often:
`mv amz_reviews /usr/local/bin`

#### using the scraper

simply:
`amz_reviews <asin> <page_start> <page_end>`

if you did not move the file to an executable path, run it via `./amz_reviews <asin> <page_start> <page_end>` from the directory to which you saved the scraper code.

**scraper parameters**
`asin` is Amazon's product identifier, which you can grab from any product page. parameters `page_start` and `page_end` are optional.

**output**
your terminal will produce a live log of scraping progress, which autosaves every 50 reviews. the finished result will be a CSV report inside the directory from which you ran the scraper.
