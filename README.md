# Web scraper for Amazon

# Notes
1. Followed the netinstructions, and got reddit scraper to work. The others (hacker news and buzzfeed) are getting 200 status error messages, indicating endpoint error.
1. Amazon book page can be scraped: 

* Name (product title):  `document.getElementById("productTitle").innerHTML`
* Description: `document.getElementById("iframeContent").innerHTML` 

* (Updated) `$('iframe#bookDesc_iframe').contentDocument.body.childNodes[1].innerHTML`
* (Updated) `$('iframe#bookDesc_iframe').contentDocument.body.childNodes[1].textContent`
* (Another) `$('#bookDesc_iframe').contentDocument.childNodes[0].childNodes[1].childNodes[1].innerHTML`

* Product dimension & Weight (shipping weight) can be found, but has to be manually extracted.
* Image URLs (pending)

1. Use the ASIN/ISBN: if 10 digit numeric code and not alphanumeric, it can safely be assumed the associated product is a book. 

# Useful tips
* `Object.getOwnPropertyNames(object)`
* `Ctrl+U` in the browser will show open `view-source` of the rendered page, which reflects closely what jQuery/cheerio is working with.
* Firefox dev console is slightly better in displaying the output in cascading format.

# References
* Simple web scraping with Node.js / JavaScript ([netinstructions](http://www.netinstructions.com/simple-web-scraping-with-node-js-and-javascript/))
* Scraping the Web With Node.js ([scotch.io](https://scotch.io/tutorials/scraping-the-web-with-node-js))
* Introduction to Webcrawling (with Javascript and Node.js) ([Medium](https://medium.com/of-all-things-tech-progress/introduction-to-webcrawling-with-javascript-and-node-js-f5a3798ee8ac))