---
title: Simple Web Scraping using Browswer
comments: True
---

If you want to quickly scrape some data from any website and don't want to go to the lengths of writing a web scraper all you need to do is

 1. Open your desired web page e.g. [Product Hunt](https://www.producthunt.com/e/0-design-tools)
 2. Scroll completely to load the page completely.
 3. Right click on any element you want to list
 
 ![](<../images/inspect_element.png>)
 
 4. Copy the class of the item
 
 ![](<../images/inspect_element_select_class.png>)
 
 5. Open Console
 6. Paste the following code to get all such elements by class 
 
 ``` javascript
 items = document.getElementsByClassName("<CLASS NAMES>") 
 ```
 
 7. Then simply loop over to get the text like following
 
 ``` javascript
 for (var i = 0; i < asdf.length ; i++){ 
     console.log(asdf[i].innerText)
 } 
 ```
 
 Iterate over this to get the desired result. You may need to adjust your class name if the item doesn't have any class and get the class name of the parent `div` or `span`.
