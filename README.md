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
|opinion ID|div.js_product-review:not(.user-post--highlight)|opinion|
|opinion ID|data-entry-id|opinion_id|
|author|user-post-author-name|author|
|recommendation|spam.user-post__author-recomendation > em|recomendation|
|number of stars|spam-user-post_score-count|stars|
|opinion’s content|div.user-post_text|content|
|list of advantages|div.review-ffeature__item--positive|pros|
|list of disadvantages|div.review-feature__item--negative|cons|
|for how many helpful|button.vote-yes[data-total-vote]|vote_yes|
|for how many unhelpful|button.vote-no[data-total-vote]|vote_no|
|publishing date|span.user-post__published > time:nth-child(1)[datetime]|published|
|Purchase date|span.user-post__published > time:nth-child(2)[datetime]|purchase|