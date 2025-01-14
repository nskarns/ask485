# Ask485
This is a search engine where the results shown are based on the words used in the search and the PageRank selected. The possible search results are a subset of Wikipedia pages.

## Development Process
This project was broken up into three main parts: Inverted Index, Index Server, and Search Engine Frontend.

### Inverted Index
Using a bunch of Wikipedia pages, we would go through (with automation) and find all of the words within the page. After collecting all of the words, we would use MapReduce to find we would count up the total count of each word within a page. This result is the inverted index that'll help us decided how much a website is related to a user's search. If the user's search has more words that are mentioned in the page, the page is going to be higher in the results.

### Index Server
The index server takes the user's search query returns a JSON with the resulting pages that will show up as the search result. The server determines the search result based on the inverted index and the PageRank value. The inverted index finds the pages with the most amount of words that were used in the user's search. The PageRank will boost a page in the search results if the page is more important. A page is more important if important pages have links to the selected page. Again, after determing the search order it sents the search order in JSON format to the search engine frontend.

### Search Engine Frontend
The search engine frontend allows the user to type and then search for something while allowing the user to choose a PageRank weight based on a slider value. After a user search and the return of results from the index server, the search engine shows the pages in order of important with clickable links.

## Features
This works exactly as Google or Bing. You input what you want to search, choose how imporant you want the PageRank to be and then search!

## Examples of Search Engine
The code for this project isn't available due to Honor Code policies, however are photos of my team's project is in this Github repository.

### 'Hello World' Search with Normal PageRank
![Hello World (Normal Page Rank)](https://github.com/nskarns/ask485/blob/main/1.png)

### 'Hello World' Search with High PageRank
![Hello World (High Page Rank)](https://github.com/nskarns/ask485/blob/main/3.png)

### 'Nicholas Karns' Search with Normal PageRank
![My Name In The Search](https://github.com/nskarns/ask485/blob/main/2.png)
