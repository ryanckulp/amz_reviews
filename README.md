## Amazon Review Scraper
download a CSV of up to 5,000 reviews for any Amazon product. video tutorial for non dorks is [here]([url](https://twitter.com/ryanckulp/status/1657434781708066821)).

#### installation
first [install Ruby](https://install.founderhacker.com/steps/choose_os). then ensure the following Ruby gems are installed (`gem install <gem_name>`):

* `watir`
* `headless`

next (optional), move the `amz_reviews` file (from this repo) to an executable path. for Mac users this is often:

`mv amz_reviews /usr/local/bin`

note: this scraper uses Firefox by default. to switch to Chrome, replace `:firefox` with `:chrome` in the code but be forewarned - you may run into headaches. KISS.

#### using the scraper

simply:
`amz_reviews <asin> <page_start> <page_end>`

(if you did not move the `amz_reviews` code to an executable path, run it via `./amz_reviews <asin> <page_start> <page_end>` from the directory in which you saved it)

scraper parameters

* `asin` is Amazon's product identifier, which you can grab from any product page
* `page_start` and `page_end` are optional; Amazon returns up to 500 pages, or 5,000 reviews

**output**

your terminal will produce a live log of scraping progress, which autosaves every 50 reviews. the finished result will be a CSV report inside the directory from which you ran the scraper.

sample report from `asin` "B07C7FS86W"

![image](https://github.com/ryanckulp/amz_reviews/assets/3083888/2b2561ec-7a0d-40e8-ab23-7307c9077943)
