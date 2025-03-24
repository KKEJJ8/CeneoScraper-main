# CeneoScraper
https://www.ceneo.pl/84514582#tag=OneClickSearch
## Ceneo scraping algorythm
1. Analysys of the structure of the webside
2. Sending http request to access first page with options
3. Cheking the code of https responce
4. Parse the html code of the first page with options
5. Extract required data from parsad code
6. If there are more pages, move to the next page and repeat step 2-5 for it
7. Save extracted data

## Analysis of the structure of the webpage
|Component|Selector|Variable|
|---------|--------|--------|
|opinion ID|#opinion-ID | |
|author|.author||
|recommendation|.recommendation||
|number of stars|.star .rating||
|opinion’s content|.opinion-content||
|list of advantages|.advantages li||
|list of disadvantages|.disadvantages li||
|for how many helpful|.helpful-count||
|for how ,ane unhelpful|.unhelpful-count||
|publishing date|.publish-data||
|Purchase date|.purchase-data||